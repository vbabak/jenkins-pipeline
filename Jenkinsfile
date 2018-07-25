pipeline {
  agent any
  stages {
    stage('step 1') {
      steps {
        sh 'sleep 1'
        sh 'exit 1'
      }
    }
    stage('step 2') {
      parallel {
        stage('step 2') {
          steps {
            sh 'sleep 1'
            sh 'sleep 2'
          }
        }
        stage('step 1 fails') {
          steps {
            echo 'Step 1 failed'
          }
        }
      }
    }
  }
}