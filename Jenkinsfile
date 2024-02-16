pipeline {
    agent any

    stages {
        stage('cleanup'){
            steps{
                echo 'Cleaning up'
                sh 'ls'
                bash 'cleanup.sh'
                echo 'Cleanup finished'
            }
        }
    }
        stage('Build Flask App') {
           steps {
                //Build the Docker image
               sh "docker rn -f $(docker ps -aq) || true"
               sh "docker create network flasknetwork || true"
               sh "docker build -t flask-app ."
               sh "docker build -t nginx1 -f Dockerfile.nginx ."  
                }
            }
    }


