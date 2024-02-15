pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building a pipeline'
                sh 'ls'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing'
                sh 'pwd'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the pipeline'
                sh 'touch deploy.txt'
            }
        }
    }
}
