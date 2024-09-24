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
                sh 'sudo pwd && sudo ls -la'
                sh 'cd /home/tayyab/taskss && git pull && pm2 restart app'
            }
        }      
    }
}
