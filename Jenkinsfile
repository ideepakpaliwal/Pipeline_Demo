pipeline {
  agent none
  
  stages {
      stage('Build') {
        agent any
        steps {
            sh 'echo "this is a build stage!!! "'
            
            sh '''
              echo "This is multiline echo"
              ls -lah
            
            '''
        }
      }
    
    stage("Docker Build") {
      agent { dockerfile true }
      steps {
          sh 'node --version'
          sh 'mvn --version'
      }
    }
  /*  stage('Back-End') {
      agent { docker { image 'maven:3-alpine' } }
        steps {
          sh 'mvn --version'
        }
      }
    stage('Front-End') {
      agent { docker {image 'node:7-alpine'} }
      steps {
        sh 'node --verison'
      }
    
    } */

    stage('Test') {
      agent any
      steps{
        sh 'echo "This is Testing Block"'

    }
  }
}

}

