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
                app = docker.build("python-app-todo")
            }
        }
        stage('Run Tests') {
            steps {
                app.inside{
                    sh 'echo Test Passed'
                }
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
