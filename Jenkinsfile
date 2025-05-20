pipeline {
    agent any

    environment {
        VENV = 'venv'
    }

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t saireddie45/app1 .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push saireddie45/app1'
            }
        }

        stage('Install Python Requirements') {
            steps {
                sh '''
                    python3 -m venv $VENV
                    . $VENV/bin/activate
                    pip install --upgrade pip
                    pip install -r requirements.txt wheel
                '''
            }
        }

        stage('Lint') {
            steps {
                script {
                    echo "This is my Linting Step"
                }
            }
        }

        stage('Test') {
            steps {
                sh '''
                    . $VENV/bin/activate
                    pytest --cov=app --junitxml=pytest-results.xml tests/
                '''
            }
        }

        stage('Run Application') {
            steps {
                script {
                    echo "This is my Run application Step"
                }
            }
        }

        stage('Verify Docker Installation') {
            steps {
                sh 'docker --version'
            }
        }
    }
}
