pipeline {
  agent any
  stages {
     stage ('Build') {
         steps {echo 'building'}
      }
      stage ('Test') {
         parallel {
              stage('unit') {steps {sh 'echo unit tests' }}
              stage('Integreation') { steps { sh 'echo Integration tests' }}

      stage ('approve') {
        steps {
           input message: 'Deploy to production?'
        }
      }
    }
  }       
} 
  
    
