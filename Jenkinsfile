pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/edgelock/jenkinsSonarQube.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'echo "Build process simulated here."'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "Test process simulated here."'
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: '**/*', fingerprint: true
            }
        }
    }
}
