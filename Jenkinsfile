pipeline {
  agent any
  stages {
    stage('step 1') {
      steps {
        sh 'sleep 1'
        sh 'echo env.BRANCH_NAME'
      }
    }
    stage('Test') {
      steps {
        echo 'Testing is OK'
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
        stage('step 2 parallel') {
          steps {
            echo 'Step 2 parallel'
            sh 'exit 0'
          }
        }
      }
    }
  }
}