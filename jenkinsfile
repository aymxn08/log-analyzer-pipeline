pipeline {
    agent any

    stages {
        stage('Run Python Script') {
            steps {
                bat '"C:\\Users\\HIS\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" analyzer.py'
            }
        }

        stage('Archive Report') {
            steps {
                archiveArtifacts artifacts: 'report.txt', fingerprint: true
            }
        }
        stage('Check Python') {
            steps {
                bat '"C:\\Users\\HIS\\AppData\\Local\\Programs\\Python\\Python314\\python.exe" --version'
            }
        }
    }
}