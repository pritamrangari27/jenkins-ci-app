pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                echo 'Cloning Code'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t jenkins-ci-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker stop jenkins-app || exit 0'
                bat 'docker rm jenkins-app || exit 0'
                bat 'docker run -d --name jenkins-app -p 5000:5000 jenkins-ci-app'
            }
        }

    }
}