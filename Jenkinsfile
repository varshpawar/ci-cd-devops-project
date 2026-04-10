pipeline {
    agent any

    stages {

        stage('Git Checkout') {
            steps {
                git 'https://github.com/varshpawar/ci-cd-devops-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t ci-cd-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8080:80 ci-cd-app'
            }
        }
    }
}