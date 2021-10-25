// pipeline {
//   agent any 
//   environment {
//         AWS_ACCOUNT_ID="367359144602"
//         AWS_DEFAULT_REGION="us-east-1" 
//         IMAGE_REPO_NAME="node-website"
//         IMAGE_TAG="IMAGE_TAG"
//         REPOSITORY_URI = "${AWS_ACCOUNT_ID}.dkr.ecr.${AWS_DEFAULT_REGION}.amazonaws.com/${IMAGE_REPO_NAME}"
//     }
  
//   stages {

//     stage('Declaring Variables') {
//       steps {
//         script {
//           env.first_name = "Mohamed"
//           env.last_name = "Ashik"
//           echo "My name is ${env.first_name} ${env.last_name}"
//           echo "REPOSITORY URI -- ${REPOSITORY_URI}"
//         }
//       }
//     }
      
//     stage('build') {
//       steps {
//         echo "Hello World"
//         sh 'docker build -t node-website .'
//       }
//   }
//     // stage('deploy') {
//     //   steps {
//     //     sh 'docker run -d -p 7000:7000 myapp:latest'
//     //   }
//     // }
//     stage('Pushing to ECR') {
//       steps {
//         script {
//           echo "Pushing build to ECR repository"
//           sh "aws ecr get-login-password --region us-east-1 | docker login --username AWS --password-stdin 367359144602.dkr.ecr.us-east-1.amazonaws.com"
//           sh "docker tag node-website:latest ${REPOSITORY_URI}"
//           sh "docker push ${REPOSITORY_URI}"
//         }
//       }
//     }
//   }
// }

pipeline {
  agent any
  stages {
    stage('run node') {
      steps {
        sh '''
          ls 
          pwd
        '''
      }
    }
  }
}
