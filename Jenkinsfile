pipeline {
  agent any
  stages {
    stage('file_create') {
      steps {
        sh '''echo \'i am batman\' > bat.txt
echo \'hello batsy\' > joker.txt'''
      }
    }

    stage('stash_file') {
      steps {
        stash(name: 'bat_stash', includes: 'bat.txt')
      }
    }

    stage('unstash_file') {
      steps {
        unstash 'bat_stash'
        sh 'cat bat.txt'
      }
    }

  }
}