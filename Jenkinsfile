//pipeline {
//  agent any
//  stages {
//    stage('step 1') {
//      steps {
//        sh 'sleep 1'
//      }
//    }
//    stage('Test') {
//      steps {
//        echo 'Testing is OK'
//      }
//    }
//    stage('step 2') {
//      parallel {
//        stage('step 2') {
//          steps {
//            sh 'sleep 1'
//            sh 'sleep 2'
//          }
//        }
//        stage('step 2 parallel') {
//          steps {
//            echo 'Step 2 parallel'
//            sh 'exit 0'
//          }
//        }
//      }
//    }
//  }
//}

node {
  stage('step 1') {
    if (env.BRANCH_NAME == 'task1') {
      echo 'I only execute on the task1 branch'
      sh 'sleep 1'
    }
  }
}

