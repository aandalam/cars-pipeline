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
        bat 'set'
      }
    }
    stage('Deploy') {
      steps {
        bat 'set'
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