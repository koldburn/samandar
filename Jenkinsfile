pipeline {
  agent any
  stages {
    stage('file_create') {
      steps {
        sh '''echo \'i am batman\' > bat.txt
echo \'hello batsy\' > joker.txt'''
      }
    }

    stage('approval_stage') {
      steps {
        input(message: 'please approve by clicking \'thats fine buddy\'', ok: 'thats fine buddy')
      }
    }

    stage('get_file_Content') {
      steps {
        sh 'echo bat.txt'
      }
    }

  }
}