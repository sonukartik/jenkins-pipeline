pipeline {
    agent any
    stages {
        stage('Clone repo') {
            steps {
                git branch: 'main', url: 'https://github.com/sonukartik/jenkins-pipeline.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
    }
}
