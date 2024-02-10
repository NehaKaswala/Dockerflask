pipeline {
    agent any
    stages {
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
