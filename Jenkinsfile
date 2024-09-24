pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/tayyabsattar042/Thesimplenodejsapplication.git'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp -r /var/lib/jenkins/workspace/simplenodejsapplicationn/app.js /var/www/html/simplenodejsapplication/'
            }
        }
        stage('Run PM2') {
            steps {
                sh 'pm2 start app.js'
            }
        }
      
    }
}
