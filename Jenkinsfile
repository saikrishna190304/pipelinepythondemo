pipeline {
    agent any

    stages {
        stage('Setup') {
            steps {
                sh '''
                    python3.10 --version
                    python3.10 -m pip install --upgrade pip setuptools
                '''
            }
        }

        stage('Lint') {
            steps {
                echo 'Running lint...'
                // Replace with your actual lint command if you have one
                sh 'flake8 .'  
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'pytest'  // Replace with your test command
            }
        }

        stage('Build') {
            steps {
                echo 'Building package...'
                sh 'python3.10 setup.py sdist bdist_wheel'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging environment...'
                // Your deploy commands here
            }
        }
    }
}
