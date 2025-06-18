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
                sh 'docker build -t my-image-name .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 --name my-container my-image-name'
            }
        }
    }

    post {
        always {
            // Optional: Stop and remove container after job finishes
            sh '''
                docker stop my-container || true
                docker rm my-container || true
            '''
        }
    }
}
