pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    // Build a Docker image with a specific tag
                    def customImage = docker.build("containous/whoami:latest")
                }
            }
        }
        stage('Run Docker Container') {
            steps {
                script {
                    // Run the Docker container exposing it on port 4444
                    sh '''
                    docker stop whoiam || true
                    docker rm whoiam || true
                    docker run -d --name whoiam -p 4444:80 containous/whoami:latest
                    '''
                }
            }
        }
        stage('Verify Deployment') {
            steps {
                script {
                    // Test the running container
                    sh '''
                    curl -f http://localhost:4444 || (echo "Container not running!" && exit 1)
                    '''
                }
            }
        }
    }
}
