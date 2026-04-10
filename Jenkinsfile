pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git branch: 'main', url: 'git 'https://github.com/varshpawar/ci-cd-devops-project.git''
            }
        }

        stage('Build') {
            steps {
                echo 'Build from Jenkinsfile successful'
            }
        }

    }
}
