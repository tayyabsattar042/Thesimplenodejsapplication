pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                script {
                    dir ('/var/www/html/simplenodejsapplication') {
                        sh 'git pull origin master'
                    }
                }
            }
        }
        stage('Run PM2') {
            steps {
                script {
                    dir ('/var/www/html/simplenodejsapplication') {
                        sh 'pm2 restart app'
                    }
                }
            }
        }
    }
}
