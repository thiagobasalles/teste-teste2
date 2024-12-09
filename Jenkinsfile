pipeline {
    agent any
    stages {
        stage('Executar Whoami') {
            steps {
                script {
                    echo 'Executando o container containous/whoami'
                    docker { image 'node:22.12.0-alpine3.20' }
                }
            }
        }
    }
}

