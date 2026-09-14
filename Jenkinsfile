pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t mynginx:latest .'
            }
        }
    }

    post {
        success {
            echo 'Docker image built successfully!'
        }

        failure {
            echo 'Build failed!'
        }
    }
}
