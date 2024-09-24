pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/tayyabsattar042/Thesimplenodejsapplication.git'
            }
        }
        stage('Deploy') {
            steps {
                sh 'sudo cp -r /var/lib/jenkins/workspace/simplenodejsapplicationn/* /var/www/html/simplenodejsapplication/'
            }
        }
        stage('Run PM2') {
            steps {
                sh 'pm2 restart all'
            }
        }
      
    }
}
