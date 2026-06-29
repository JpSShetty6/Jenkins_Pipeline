pipeline {
    agent any

    stages {

        stage('Docker Build') {
            steps {
                sh 'docker build -t python-demo .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run python-demo'
            }
        }
    }
}
