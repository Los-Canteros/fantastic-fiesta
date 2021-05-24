pipeline {
    agent {
      docker {
        image 'python:3.8-slim'
      }
    }

    stages {
        stage('Python') {
            steps {
                publishChecks detailsURL: 'htpps://rti.com', name: 'Testing', status: 'IN_PROGRESS', title: 'Testing'
                sh 'python --version'
            }
            
            post {
                success {
                    publishChecks detailsURL: 'htpps://rti.com', name: 'Testing', title: 'Testing'
                }
                failure {
                    publishChecks conclusion: 'FAILURE', detailsURL: 'htpps://rti.com', name: 'Testing', title: 'Testing'
                }
            }
        }
    }
}
