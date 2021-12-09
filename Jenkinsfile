pipeline {
  agent any
  stages {
    stage('Build Jar') {
      steps {
        sh '''./mvnw package
pwd'''
        stash 'Target'
      }
    }

    stage('Execute Jar') {
      steps {
        unstash 'target'
        sh 'java -jar target/*jar'
      }
    }

  }
}