pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''date
              pwd'''
      }
    }

    stage('Testing') {
      parallel {
        stage('Test') {
          steps {
            echo 'Test msg1'
          }
        }

        stage('Test Par') {
          steps {
            echo 'Test param'
          }
        }

      }
    }

    stage('Deploy') {
      input {
        message 'Good to Deploy prod?'
      }
      steps {
        echo 'Deployment'
        sleep 60
      }
    }

  }
}