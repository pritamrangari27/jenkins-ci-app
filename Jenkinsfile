pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh 'echo Build Successful'
            }
        }

        stage('Deploy') {
            steps {
                sh 'nohup python3 app.py > output.log 2>&1 &'
            }
        }

    }
}