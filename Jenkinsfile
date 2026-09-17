pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/Yathran123/Student-Management-Archive-Artifacts.git'
            }
        }

        stage('Generate Report') {
            steps {
                bat 'C:/Users/SENTHIL/AppData/Local/Programs/Python/Python313/python.exe app.py'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt',
                    fingerprint: true
            }
        }
    }
}