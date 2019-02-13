pipeline {
  agent any
  stages {
    stage('unit/Shell ') {
      steps {
        sh '''SET PATH=%C:\\apache-maven-3.5.2\\bin%;
mvn clean test'''
      }
    }
    stage('integration test') {
      steps {
        sh 'echo "integration test"'
      }
    }
    stage('UI tests') {
      steps {
        build(job: 'Smoke_UI_Test', propagate: true, wait: true)
      }
    }
  }
}