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
        unstash 'target'
        sh 'java -jar target/*jar'
      }
    }

  }
}