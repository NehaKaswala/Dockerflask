pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t flask-app .'
            }
        }
        stage('Push to Registry') {
            steps {
                sh 'docker push https://hub.docker.com/u/nehakaswala/flask-app'
            }
        }
    }
}
