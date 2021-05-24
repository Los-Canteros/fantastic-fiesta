pipeline {
    agent {
      docker {
        image 'python:3.8-slim'
      }
    }

    stages {
        stage('Python') {
            steps {
                withChecks('Testing') {
                    sh 'python --version'
                }
            }
        }
    }
}
