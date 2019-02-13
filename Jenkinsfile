pipeline {
  agent any
  stages {
    stage('unit test') {
      steps {
        bat 'echo "Unt tests"'
      }
    }
    stage('integration test') {
      steps {
        sh 'echo \'Integration tests are running\''
      }
    }
    stage('UI tests') {
      steps {
        build(job: 'Smoke_UI_Test', propagate: true, wait: true)
      }
    }
  }
}