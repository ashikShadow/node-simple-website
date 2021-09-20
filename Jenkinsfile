pipeline {
  agent any 
  
  stages {
    stage('build') {
      steps {
        echo "Hello World"
        sh 'docker build -t myapp .'
        sh 'docker run -d myapp:latest'
      }
    }
  }
}
