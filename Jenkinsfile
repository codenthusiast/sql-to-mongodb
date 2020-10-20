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
                sh 'node index.js --sqlConnectionString="Data Source=host.docker.internal:1443;User Id=gafar.popoola;Password=Password@123;Initial Catalog=IdentityServer;Integrated Security=True" --mongoConnectionString="mongodb://host.docker.internal:27017" --targetDatabaseName="IdentityServer2" --skip="Consents,Tokens" --remapKeys' 
            }
        }
    }
}