pipeline {
    agent any
    stages {
        stage ('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com'
            }
        }
        stage ('Generate Report') {
            steps {
                // This uses your exact Python launcher path from your cmd screen
                bat '"C:\\Users\\NIVEDHA\\AppData\\Local\\Programs\\Python\\Launcher\\py.exe" app.py'
            }
        }
        stage ('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
    }
}
