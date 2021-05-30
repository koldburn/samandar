pipeline {
  agent any
  stages {
    stage('first_stage') {
      steps {
        sh '''chmod +x ./java/build.sh
./java/build.sh'''
      }
    }

    stage('archiveArtifacts') {
      steps {
        archiveArtifacts(artifacts: 'java/*.class', fingerprint: true)
      }
    }

  }
}