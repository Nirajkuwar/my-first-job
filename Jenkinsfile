pipeline {
    agent any
    parameters {
        choice(name: 'ENIRONMENT', choices: ['staging', 'production'], description: 'Target')
    }
    stages {
        stage('deploy') {
            steps{
                sh 'echo Deploying to ${ params.ENVIRONMENT }
            }
         }
     }
}
    
    
        
