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
        bat 'echo "Integration test"'
      }
    }
    stage('UI tests') {
      steps {
        build(job: 'Smoke_UI_Test', propagate: true, wait: true)
      }
    }
    stage('Final stage') {
      steps {
        bat 'echo "The end"'
      }
    }
  }
}