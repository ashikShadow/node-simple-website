pipeline {
  agent any 
  
  stages {
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
