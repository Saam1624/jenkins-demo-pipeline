pipeline {

    agent {
        docker {
            image 'python:3.12'
        }
    }

    environment {
        HOME = "/tmp"
        PATH = "/tmp/.local/bin:${env.PATH}"
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh 'pip install --user -r requirements.txt'
            }
        }

        stage('Run Test') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build Completed') {
            steps {
                echo 'Application Build Successful'
            }
        }

    }
}