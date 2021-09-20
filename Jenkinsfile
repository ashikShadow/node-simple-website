pipeline {
  agent any 
  
  stages {

    stage('Declaring Variables') {
      steps {
        //env.ECRREPOURI = "096176992732.dkr.ecr.ap-south-1.amazonaws.com/fego-transaction"
        //env.DOCKERPUSHURL = "https://096176992732.dkr.ecr.ap-south-1.amazonaws.com/fego-transaction"
        // echo "branch name : demo"
        // env.TAG = "${env.BRANCH_NAME}" + "-" + "${BUILD_NUMBER}"
        env.first_name = "Mohamed"
        env.last_name = "Ashik"
      }
    }
      
    stage('build') {
      steps {
        echo "Hello World"
        sh 'docker build -t myapp .'
        echo "My name is ${env.first_name} ${env.last_name}"
      }
  }
    stage('deploy') {
      steps {
        sh 'docker run -d -p 7000:7000 myapp:latest'
      }
    }
  }
}
