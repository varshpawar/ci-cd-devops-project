pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/varshpawar/ci-cd-devops-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ci-cd-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8080:80 ci-cd-app'
            }
        }

    }

    post {
        success {
            echo 'Pipeline SUCCESS 🚀 App deployed successfully'
        }
        failure {
            echo 'Pipeline FAILED ❌ Check logs'
        }
    }
}