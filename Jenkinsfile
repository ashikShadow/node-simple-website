pipeline {
  agent any 
  environment {
        AWS_ACCOUNT_ID="367359144602"
        AWS_DEFAULT_REGION="us-east-1" 
        IMAGE_REPO_NAME="node-website"
        IMAGE_TAG="IMAGE_TAG"
        REPOSITORY_URI = "${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}"
    }
  
  stages {

    stage('Declaring Variables') {
      steps {
        script {
          env.first_name = "Mohamed"
          env.last_name = "Ashik"
          echo "My name is ${env.first_name} ${env.last_name}"
          echo "REPOSITORY URI -- ${REPOSITORY_URI}"
        }
      }
    }
      
    stage('build') {
      steps {
        echo "Hello World"
        sh 'docker build -t myapp .'
      }
  }
    stage('deploy') {
      steps {
        sh 'docker run -d -p 7000:7000 myapp:latest'
      }
    }
  }
}
