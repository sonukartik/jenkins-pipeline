pipeline {
    agent any

    environment {
        IMAGE_NAME = 'my-image-name'
    }

    stages {
        stage('Clone repo') {
            steps {
                git branch: 'main', url: 'https://github.com/sonukartik/jenkins-pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build("my-image")
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    dockerImage.run("-p 5000:5000")
                }
            }
        }
    }
}
