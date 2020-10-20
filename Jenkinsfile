pipeline {
    agent any
    tools {nodejs "node installation"}
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