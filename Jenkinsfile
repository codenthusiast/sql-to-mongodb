pipeline {
    agent {
        docker {
            image 'node:14.14.0-alpine3.11' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Execute') { 
            steps {
                sh '$source' 
            }
        }
    }
}