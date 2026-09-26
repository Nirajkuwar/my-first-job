pipeline {
  agent any
  parameters{
    choice( name: 'ENVIRONMENT' , choices: ['staging', 'production'], description: 'Target')
  }
  stages {
    stage("Build") { steps { sh 'echo Building' }}
    stage ('Test') {
      parallel {
        stage('Unit') { 
          steps { 
            sh 'echo Unit Testing'
          }
        }
        stage('Integration') { 
          steps {
            sh 'echo Integration Testing'
            }
          }
        }
      }
      stage('Approve') {
         when { expression { params.ENVIRONMENT == 'production' } }
         steps {
          input message: 'Deploy to production?'
        }
      }
      stage ('Deploy') { 
        steps { 
          sh "echo deploying to ${params.ENVIROMENT} " 
        }
      }
    }
}
      
  
