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
                    
                    sh 'docker ps | grep whoami'
                }
            }
        }
    }
}