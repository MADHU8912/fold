pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/YOURNAME/devops-docker-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t devops-site .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 8080:80 devops-site'
            }
        }

    }
}