pipeline{
  agent any
  stages{
    stage('Clone repo'){
      steps{
        git 'https://github.com/sonukartik/jenkins-pipeline.git'
      }
    }
       stage('Build Docker Image') {
            steps {
                script {
                    dockerImage = docker.build("my-flask-app")
                }
            }
        }
        stage('Run Container') {
            steps {
                script {
                    dockerImage.run('-p 5000:5000')
                }
            }
        }
    }
}
