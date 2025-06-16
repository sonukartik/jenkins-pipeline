pipeline {
    agent any

    stages {
        stage('Clone repo') {
            steps {
                git branch: 'main', url: 'https://github.com/sonukartik/jenkins-pipeline.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image and save to variable
                    dockerImage = docker.build("my-image-name")
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    // Run the image exposing port 5000
                    dockerImage.run("-p 5000:5000")
                }
            }
        }
    }
}
