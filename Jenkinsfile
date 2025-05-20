pipeline {
    agent {
        docker {
            image 'python:3.10' // Pulls official Python image from Docker Hub
        }
    }

    stages {
        stage('Setup') {
            steps {
                sh 'python -m pip install --upgrade pip'
            }
        }

        stage('Lint') {
            steps {
                echo 'Linting code (placeholder)...'
                // e.g., sh 'flake8 .'
            }
        }

        stage('Test') {
            steps {
                sh 'pip install pytest'
                sh 'pytest'
            }
        }

        stage('Build') {
            steps {
                echo 'Build step (placeholder)...'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging (placeholder)...'
            }
        }
    }
}
