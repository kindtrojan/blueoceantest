pipeline {
  agent any
  stages {
    stage('stage1') {
      steps {
        sh 'who'
        echo 'printing the currently logged in user'
      }
    }

    stage('stage2') {
      parallel {
        stage('stage2_1') {
          steps {
            sh 'date'
          }
        }

        stage('stage2_2') {
          steps {
            echo 'gonna print date parallel to this'
          }
        }

      }
    }

    stage('stage3') {
      steps {
        sleep 2
        echo 'just gonna sleep for 2 seconds'
      }
    }

  }
}