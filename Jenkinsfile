pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    cd ('/var/www/html/simplenodejsapplication') {
                        sh 'git pull origin master || echo "Failed to pull from git"'
                    }
                }
            }
        }
        stage('Run PM2') {
            steps {
                script {
                    cd ('/var/www/html/simplenodejsapplication') {
                        sh 'pm2 restart app'
                    }
                }
            }
        }
    }
}
