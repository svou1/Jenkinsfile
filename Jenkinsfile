pipeline {
    agent any

    stages {
        stage('cleanup') {
            steps {
                echo 'Cleaning up'
                sh 'docker ps -aq | xargs docker rm -f || true'
                echo 'Cleanup finished'
            }
        }

        stage('Build Flask App') {
            steps {
                // Build the Docker images
                sh 'docker build -t flask-app .'
                sh 'docker build -t nginx1 -f Dockerfile.nginx .'
            }
        }
        stage('Run Flask App') {
            steps {
                sh "docker run --name -d flask-app --network flasknetwork flask-app"
                sh "docker run --name nginx -d -p 80:80 -f Dockerfile.nginx --network flasknetwork nginx1"
            }    
        }
    }
}
