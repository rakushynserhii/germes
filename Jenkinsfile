pipeline {
  agent any
  stages {

    stage('unit test') {
      steps {
        withEnv(["PATH+EXTRA=/usr/local/bin"]) {
          sh 'mvn clean test'
        }
      }
    }

    stage('integration test') {
      steps {
        sh 'echo \'Integration tests are running\''
      }
    }

    stage('UI tests') {
      steps {
        build(job: 'UI_Testing', propagate: true, wait: true)
      }
    }
  }
}