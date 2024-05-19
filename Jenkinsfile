pipeline {
    agent any

    stages {
        stage('Limpiar Workspace') {
            steps {
                // usando el intérprete de comandos pwsh
                pwsh 'Remove-Item -Path ./*'
            }
        }

        stage('Primera linea') {
            steps {
                sh 'echo "Primera linea del archivo" > archivo.txt'
            }
        }

        stage('Segunda linea') {
            steps {
                // usando el intérprete de comandos pwsh
                pwsh 'Add-Content -Value "Segunda linea del archivo" -Path archivo.txt'
                sh 'cat archivo.txt'
            }
        }
    }
}