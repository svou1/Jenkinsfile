pipeline {
    agent any

    stages {
       stage('Build Docker Image') {
           steps {
                //Build the Docker image
               docker.build('dockerimage', '-f Dockerfile.txt . '
                }
                            }
                            }
                            }
        stage('Build') {
            steps {
                echo 'Buid Docker Image'{

                //Run the Docker container
                docker.image('dockerimage').run('-p 8080:80, '--name container')
                    }    
                }        
            }    
        }
    }


