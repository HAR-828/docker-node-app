pipeline {
    agent any

    stages {

        stage('Pull Code') {
            steps {
                echo 'Pulling code from GitHub...'
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                echo 'Building Docker image...'
                sh 'docker build -t docker-node-app:latest .'
            }
        }

        stage('Display Image Details') {
            steps {
                echo 'Docker image details:'
                sh 'docker images docker-node-app'
            }
        }
    }
}
