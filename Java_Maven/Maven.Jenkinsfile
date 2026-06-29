pipeline {

    agent any

    tools {
        maven 'Maven3'
        jdk 'JDK21'
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

	stage('Build') {
    		steps {
        		dir('Java_Maven') {
            		sh 'mvn clean package'
        		}	
 		}
	}

    }

    post {

        success {
            echo 'Maven Build Successful'
        }

        failure {
            echo 'Build Failed'
        }

    }

}
