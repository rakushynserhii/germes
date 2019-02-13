pipeline {
  agent any
  stages {
    stage('unit') {
      steps {
        sh '''mvn clean test
'''
      }
    }
  }
}