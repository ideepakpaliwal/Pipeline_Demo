pipeline {
  agent any
  
  stages {
      stage('Build') {
        steps {
            sh 'echo "this is a build stage!!! "'
            
            sh '''
              echo "This is multiline echo"
              ls -lah
            
            '''
        }
      } 
    }
}
