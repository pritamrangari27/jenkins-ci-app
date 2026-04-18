pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning Code'
            }
        }

        stage('Build') {
            steps {
                sh 'docker --version || true'
                sh 'echo Build Successful'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo Deployment Successful'
            }
        }

    }
}