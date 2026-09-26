pipeline {
  agent any
  environment {
    APP_ENV = 'Test'
  }
  stages {
    stage('checkout') {
      steps {
        sh 'echo Building'
      }
    }
    stage('test') {
      steps {
        sh ''echo Running test'
      }
    }
  }
  post {
     success {
       echo 'All stages passed'
     }
    failure {
      echo 'something failed'
    }
  } 
}  
        
