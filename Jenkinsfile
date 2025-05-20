pipeline {
    agent any

    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t minfyakhilesh/app1 .'

            }
        }
        stage ("pushing") {
            steps {
            sh 'docker push minfyakhilesh/app1'
        }

    }
}
}
