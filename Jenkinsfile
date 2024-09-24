pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Change directory to the application folder
                    dir('/var/www/html/simplenodejsapplication') {
                        // Pull the latest changes from the repository
                        sh 'git pull origin master || echo "Failed to pull from git"'
                    }
                }
            }
        }
        stage('Run PM2') {
            steps {
                script {
                    // Change directory to where the app.js is located
                    dir('/var/www/html/simplenodejsapplication') {
                        // Restart the app using PM2
                        sh 'pm2 restart app || pm2 start app.js --name app || echo "Failed to restart or start PM2 app"'
                    }
                }
            }
        }
    }
}
