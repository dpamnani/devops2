pipeline {
  agent any
  stages {
    stage('Build Jar') {
      steps {
        sh '''./mvnw package
pwd'''
        stash 'target'
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