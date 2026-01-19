pipeline {
    agent any

    tools {
        nodejs 'node18'
    }

    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/<username>/express-frontend.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Restart Express') {
            steps {
                sh 'pm2 restart express-frontend || pm2 start app.js --name express-frontend'
            }
        }
    }
}
