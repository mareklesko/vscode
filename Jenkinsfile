pipeline {
    agent {
        docker {
            image 'nikolaik/python-nodejs:python3.9-nodejs12-alpine' 
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
