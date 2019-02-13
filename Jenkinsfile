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
    stage('UI_test') {
      steps {
        build(propagate: true, wait: true, job: 'Smoke_UI_test')
      }
    }
  }
}