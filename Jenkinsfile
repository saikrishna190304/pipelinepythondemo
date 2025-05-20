pipeline {
    agent any
    stages {
        stage('Setup') {
            steps {
                sh 'python3 -m pip install --upgrade pip'
            }
        }
        stage('Lint') {
            steps {
                echo 'Linting...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging...'
            }
        }
    }
}
