pipeline {
  agent any
  stages {
    stage('first_stage') {
      steps {
        echo 'hello neo'
        echo 'yes'
      }
    }

    stage('shell_stage') {
      steps {
        sh 'pwd'
      }
    }

    stage('folder_shell') {
      steps {
        sh '''chmod +x ./jenkins/build.sh
./jenkins/build.sh
'''
      }
    }

  }
}