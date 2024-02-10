pipeline {
    agent any
    stages {
        stage('Install Docker') {
            steps {
                sh 'curl -fsSL https://get.docker.com -o get-docker.sh'
                sh 'sh get-docker.sh'
            }
        }
        stage('Build') {
            steps {
                sh 'echo started'
                sh 'docker build -t flask-app .'
            }
        }
        stage('Push to Registry') {
            steps {
                sh 'docker push nehakaswala/flask-app:latest'
            }
        }
    }
}
