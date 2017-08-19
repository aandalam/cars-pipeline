pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'set'
      }
    }
    stage('Test') {
      steps {
        parallel(
          "Junit": {
            echo 'Hello Test'
            
          },
          "DBUnit": {
            echo 'DBUnit'
            
          }
        )
      }
    }
    stage('Deploy') {
      steps {
        parallel(
          "Deploy": {
            bat 'set'
            
          },
          "Deploy Stage": {
            sh './deploy.sh'
            
          }
        )
      }
    }
    stage('Dev') {
      steps {
        parallel(
          "Dev": {
            echo 'Hello Dev'
            
          },
          "Test": {
            echo 'Test'
            
          }
        )
      }
    }
  }
}