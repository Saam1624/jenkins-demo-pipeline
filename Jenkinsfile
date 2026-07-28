pipeline {

    agent {
        docker {
            image 'python:3.12'
        }
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh 'pip install --user -r requirements.txt'
            }
        }

        stage('Run Test') {
            steps {
                sh 'python -m pytest'
            }
        }

        stage('Build Completed') {
            steps {
                echo 'Application Build Successful'
            }
        }

    }
}