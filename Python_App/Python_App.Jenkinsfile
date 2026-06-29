pipeline {
    agent any

    stages {

	stage('Check Python') {
		steps {
        		sh 'whoami'
        		sh 'which python3 || true'
        		sh 'which pip3 || true'
        		sh 'python3 --version || true'
        		sh 'pip3 --version || true'
    			}
		}

        stage('Install') {
            steps {
                dir('Python_App') {
                    sh 'python3 --version'
                    sh 'pip3 install -r requirements.txt'
                }
            }
        }

        stage('Run') {
            steps {
                dir('Python_App') {
                    sh 'python3 app.py'
                }
            }
        }

        stage('Test') {
            steps {
                dir('Python_App') {
                    sh 'pytest test_app.py'
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed.'
        }
    }
}
