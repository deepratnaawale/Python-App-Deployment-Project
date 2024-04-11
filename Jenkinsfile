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
                script{
                    app = docker.build("python-app-todo")   
                }
            }
        }
        stage('Run Tests') {
            steps {
                script{
                    app.inside{
                        sh 'echo Test Passed'
                    }   
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
