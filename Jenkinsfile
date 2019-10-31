pipeline {
  agent any
  stages {

    stage('integration test') {
      steps {
        sh 'echo \'Integration test are running\''
      }
    }

    stage('UI tests') {
      steps {
        build(job: 'UI_Testing', propagate: true, wait: true)
        script {
                    allure([
                            includeProperties: false,
                            jdk: '',
                            properties: [],
                            reportBuildPolicy: 'ALWAYS',
                            results: [[path: 'target/allure-results']]
                    ])
            }
      }
    }
  }
}