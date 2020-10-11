pipeline {
    agent {
        docker {
            image 'node:12.19.0-alpine3.10' 
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
