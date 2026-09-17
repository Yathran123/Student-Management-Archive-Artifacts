pipeline {
    agent any

    stages {
        stage('Run Python') {
            steps {
                bat 'C:/Users/SENTHIL/AppData/Local/Programs/Python/Python313/python.exe app.py'
            }
        }

        stage('Check Report') {
            steps {
                bat 'dir'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', allowEmptyArchive: false
            }
        }
    }
}