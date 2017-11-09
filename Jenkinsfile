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
            
          },
          "Jasmine": {
            echo 'Jasmine'
            
          }
        )
      }
    }
    stage('Browser Tests') {
      steps {
        parallel(
          "Firefox": {
            echo 'Browser Tests'
            
          },
          "Edge": {
            echo 'Edge'
            
          },
          "Safari": {
            echo 'Safari'
            
          },
          "Chrome": {
            echo 'Chrome'
            
          }
        )
      }
    }
    stage('Dev') {
      steps {
        echo 'Hello Dev'
      }
    }
    stage('Integration') {
      steps {
        echo 'Integration'
      }
    }
    stage('QA') {
      steps {
        echo 'QA'
      }
    }
    stage('Pilot') {
      steps {
        echo 'Pilot'
      }
    }
    stage('Prod') {
      steps {
        echo 'Prod'
      }
    }
    stage('Final') {
      steps {
        archiveArtifacts(artifacts: '**/*jar', excludes: 'null')
      }
    }
  }
}