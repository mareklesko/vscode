pipeline {
    agent {
        docker {
            image 'mcr.microsoft.com/vscode/devcontainers/repos/microsoft/vscode:dev' 
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
