pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                cleanWs()
                git branch: 'main', url: 'https://github.com/nivedhasvlr-collab/student-management-pipeline-2'
            }
        }
        stage ('Generate Report') {
            steps {
                // This points exactly to the working Python 3.13 directory
                bat '"C:\\Users\\NIVEDHA\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" app.py'
            }
        }
        stage ('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
