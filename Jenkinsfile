pipeline {
  agent any
  stages {
    stage('Build Jar') {
      steps {
        sh './mvnw package'
        stash 'Target'
      }
    }

  }
}