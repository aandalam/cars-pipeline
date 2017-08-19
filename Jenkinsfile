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
          "Browser Test": {
            echo 'Browser Tests'
            
          },
          "Firefox": {
            echo 'firefox'
            
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