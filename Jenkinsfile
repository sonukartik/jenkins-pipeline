pipeline {
    agent any
    stages {
        stage('Print Workspace') {
            steps {
                script {
                    echo "WORKSPACE: ${env.WORKSPACE}"
                    sh 'pwd'
                    sh 'ls -la'
                }
            }
        }
    }
}
