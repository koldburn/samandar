pipeline {
  agent any
  stages {
    stage('first_stage') {
      steps {
        echo 'hello neo'
      }
    }

    stage('archiveArtifacts') {
      steps {
        archiveArtifacts(artifacts: '/java/*.class', fingerprint: true)
      }
    }

  }
}