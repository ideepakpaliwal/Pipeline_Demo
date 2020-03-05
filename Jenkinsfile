/*pipeline {
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
    stage('Image') {
      agent {
        docker { 
          image 'node:7-alpine'
      //    image 'maven:3-alpine'
        }
      }
        steps {
          sh 'node --version'
        //  sh 'mvn --version'
        }
      }
    }
}
*/

pipeline {
    agent {
        docker { 
                image 'maven:3-alpine' 
                image 'node:7-alpine' 
           }
    }
    stages {
        stage('Test') {
            steps {
                sh 'node --version'
                sh 'mvn --version'
            }
        }
    }
}
