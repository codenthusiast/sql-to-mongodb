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
                sh 'node --max-old-space-size=4096 index.js' 
            }
        }
    }
}