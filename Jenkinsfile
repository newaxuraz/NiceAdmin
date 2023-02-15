pipeline {
    agent any


    stages {
        stage('git checkuot sample') {
            steps {
                git branch: 'main', url: 'https://github.com/newaxuraz/NiceAdmin'
            }
        }
         stage('Delete existing files') {
            steps {
                sh 'sudo rm -rf /var/www/html'
            }
        }
        stage('Copy  files') {
            steps {
                sh 'sudo cp -R /var/lib/jenkins/workspace/NiceAdmin/* /var/www/html'
            }
        }
    }
}

