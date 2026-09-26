pipeline {
  agent any
  stages {
    stage("hello") {
      steps {
         echo 'Hello, jenkins!'
        sh 'echo this runs a real shell command'
        sh 'pwd'
        sh 'ls -la'
        sh 'ls -lh'
        sh 'whoami'
      }
    }
  }
}
