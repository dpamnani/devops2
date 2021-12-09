pipeline {
  agent any
  stages {
    stage('Build Jar') {
      steps {
        sh './mvnw package'
        stash 'Target'
      }
    }

    stage('Execute Jar') {
      steps {
        unstash 'Target'
        sh 'java -jar target/*jar'
      }
    }

  }
}