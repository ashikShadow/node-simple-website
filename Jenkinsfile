pipeline {
  agent any 
  
  stages {
    stage('greet') {
      steps {
        echo "Hello World"
        script {
          sh "pwd"
          sh "sudo docker build -t node-website:1.1 .
        }
      }
    }
  }
}
