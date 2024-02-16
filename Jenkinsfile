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
                //Clone the GitLab repository
                git branch: 'main', url: 'https://gitlab.com/Reece-Elder/dockerfileexercise.git'
                sh 'touch deploy.txt'
                sh 'mv deploy.txt ~/jenkins'
            }
        }
    }
}
