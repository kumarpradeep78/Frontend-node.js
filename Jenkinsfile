pipeline {
    agent any

    tools {
        nodejs 'node18'
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Restart Express') {
            steps {
                sh '''
                pm2 restart express-frontend || pm2 start app.js --name express-frontend
                '''
            }
        }
    }
}
