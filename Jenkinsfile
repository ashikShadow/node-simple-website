pipeline {
  agent any 
  
  stages {
    stage('build') {
      steps {
        echo "Hello World"
        sh 'sudo docker build -t myapp .'
      }
    }
  }
}
