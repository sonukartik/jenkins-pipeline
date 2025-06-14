pipeline{
  agent any
  stages{
    stage('Clone repo'){
      steps{
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
                script {
                    dockerImage.run('-p 5000:5000')
                }
            }
        }
    }
}
