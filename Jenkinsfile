pipeline {
    environment {
    registry = "sotaaaaa/express-example"
    registryCredential = 'DOCKER_HUB_ACCOUNT'
    dockerImage = ''
    }

    agent any
    stages {
            stage('Building Docker Image') {
                steps {
                    sh "sudo docker build -t $registry:$BUILD_NUMBER"
                }
            }

            stage('Cleaning Up') {
                steps{
                  sh "docker rmi --force $registry:$BUILD_NUMBER"
                }
            }
        }
    }
