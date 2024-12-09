pipeline {
    agent any

    stages {
        stage('Run Docker Container') {
            steps {
                script {
                    sh 'docker run -d --name whoami -P containous/whoami'
                }
            }
        }

        stage('Verify Deployment') {
            steps {
                script {
                    // Substitua pelo seu comando de verificação (exemplo: curl ou outros testes)
                    sh 'docker ps | grep whoami'
                }
            }
        }
    }
}
