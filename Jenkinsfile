pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/varshpawar/ci-cd-devops-project.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build started'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
    }
}