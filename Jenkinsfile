pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                // This connects Jenkins directly to your NEW second repository
                git branch: 'main', url: 'https://github.com/nivedhasvlr-collab/student-management-pipeline-2'
            }
        }
        stage ('Generate Report') {
            steps {
                bat 'python app.py'
            }
        }
        stage ('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
