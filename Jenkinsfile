pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/tayyabsattar042/My-Angular-App.git'
            }
        }
        stage('Deploy') {
            steps {
                sh '/var/lib/jenkins/workspace/simplenodejsapplicationn/browser/* /var/www/html/simplenodejsapplication/'
            }
        }
        stage('Run PM2') {
            steps {
                sh 'pm2 restart all'
            }
        }
      
    }
}
