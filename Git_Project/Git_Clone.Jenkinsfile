pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Display Files') {
            steps {
                sh 'pwd'
                sh 'ls -R'
            }
        }
    }
}
