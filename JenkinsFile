pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t python-app-todo .'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'docker run -p 5000:5000 python-app-todo'
            }
        }
        stage('Deploy Application') {
            steps {
                // Add deployment steps here (e.g., push to production server)
                sh 'echo Sample Deployed'
            }
        }
    }
}
