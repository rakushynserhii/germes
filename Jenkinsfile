pipeline {
  agent any
  stages {
    stage('unit') {
      steps {
        sh '''mvn clean test
'''
      }
    }
    stage('integration') {
      steps {
        sh 'echo \'integration tests\''
      }
    }
  }
}