pipeline {
    agent any

    stages {
        stage('Setup') {
            steps {
                sh 'python3.10 --version'
                sh 'python3.10 -m pip install --upgrade pip'
            }
        }

        stage('Lint') {
            steps {
                sh 'python3.10 -m pip install pylint'
                sh 'pylint *.py || true'
            }
        }

        stage('Test') {
            steps {
                sh 'python3.10 -m unittest discover'
            }
        }

        stage('Build') {
            steps {
                echo 'Build step goes here'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploy step goes here'
            }
        }
    }
}
