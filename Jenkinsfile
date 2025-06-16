pipeline {
    agent any
    stages {
        stage('Check Docker Version') {
            steps {
                sh 'docker --version'
            }
        }

        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/sonukartik/jenkins-pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-image-name .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 my-image-name'
            }
        }
    }
}
