pipeline {
    agent {
        docker {
            image 'sitapati/docker-alpine-python-node' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'yarn && yarn run compile && yarn run compile-web' 
            }
        }
    }
}
