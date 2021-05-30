pipeline {
  agent any
  stages {
    stage('file_create') {
      parallel {
        stage('file_create') {
          steps {
            sh '''echo \'i am batman\' > bat.txt
echo \'hello batsy\' > joker.txt'''
          }
        }

        stage('o/p3') {
          steps {
            sh 'cat joker.txt'
          }
        }

      }
    }

    stage('stash_file') {
      steps {
        stash(name: 'bat_stash', includes: 'bat.txt')
      }
    }

    stage('o/p') {
      parallel {
        stage('o/p') {
          steps {
            sh 'cat bat.txt'
          }
        }

        stage('o/p2') {
          steps {
            sh 'cat bat.txt'
          }
        }

      }
    }

  }
}