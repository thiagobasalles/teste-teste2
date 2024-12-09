pipeline {
    agent any
    stages {
        stage('Executar Whoami') {
            steps {
                script {
                    echo 'Executando o container containous/whoami'
                    sh 'docker run -d -P --name iamfoo containous/whoami'
                }
            }
        }
    }
}

