# Jenkins-CI-CD-Pipeline
# Node.js Application with Jenkins CI/CD

This repository contains a simple Node.js application along with a Jenkinsfile for setting up a basic CI/CD pipeline.

## Prerequisites

1. Install Node.js: https://nodejs.org/
2. Install Docker: https://docs.docker.com/get-docker/
3. Set up Jenkins: https://www.jenkins.io/doc/book/installing/

## Running the Application Locally

1. Clone this repository: `git clone https://github.com/your-username/node-jenkins-cicd.git`
2. Navigate to the project directory: `cd node-jenkins-cicd`
3. Install dependencies: `npm install`
4. Run the application: `node app.js`
5. Open your browser and go to http://localhost:3000

## Jenkins CI/CD Pipeline

1. Create a new Jenkins pipeline job.
2. Configure the pipeline to use this repository.
3. Set up Docker Hub credentials in Jenkins (username/password).
4. Run the Jenkins pipeline.

The pipeline will build and push the Docker image to Docker Hub. The deployment stage needs to be adapted based on your deployment target (e.g., Docker host, Kubernetes cluster).

For more information, refer to the Dockerfile, Jenkinsfile, and the application code.

Happy coding!
