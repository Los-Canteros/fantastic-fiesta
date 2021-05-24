pipeline {
    agent {
      docker {
        image 'python:3.8-slim'
      }
    }

    stages {
        stage('Python') {
            steps {
                sh 'python --version'
            }
        }
    }
}
