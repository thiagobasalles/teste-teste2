pipeline {
    agent any
    stages {
        stage('Executar Docker Whoami') {
            steps {
                script {
                    echo 'Executando o container containous/whoami'
                    sh '''
                        docker ps -q --filter "name=iamfoo" | grep -q . && echo "Container já está rodando" || docker run -d -P --name iamfoo containous/whoami
                    '''
                }
            }
        }
    }
}
