pipeline {
    agent {
        docker {
            image 'saireddie45/python-jenkins:latest'
        }
    }

    environment {
        VENV = 'venv'
    }

    stages {
        stage("Install") {
            steps {
                sh '''
                    python -m venv $VENV
                    . $VENV/bin/activate
                    pip install --upgrade pip
                    pip install -r requirements.txt wheel
                '''
            }
        }

        stage("Lint") {
            steps {
                script {
                    echo "This is my Linting Step"
                }
            }
        }

        stage("Test") {
            steps {
                sh '''
                    . $VENV/bin/activate
                    pytest --cov=app --junitxml=pytest-results.xml tests/
                '''
            }
        }

        stage("Run Application") {
            steps {
                script {
                    echo "This is my Run application Step"
                }
            }
        }
    }
}
