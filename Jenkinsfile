pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout scm
                }
            }
        }

        stage('Build and Push Docker Image') {
            steps {
                script {
                    // Define your Docker Hub credentials
                    withCredentials([usernamePassword(credentialsId: 'docker-hub-credentials', passwordVariable: 'DOCKER_PASSWORD', usernameVariable: 'DOCKER_USERNAME')]) {
                        // Build and push Docker image
                        sh "docker build -t your-docker-username/node-app ."
                        sh "docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD"
                        sh "docker push your-docker-username/node-app"
                    }
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy the Docker image (you need to adapt this based on your deployment target)
                    // For example, you might deploy to a Docker host or a Kubernetes cluster
                    sh "echo Deploying the application..."
                }
            }
        }
    }
}
