pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './gradlew bootJar'
      }
    }
    stage('Test') {
      steps {
        sh './gradlew test'
      }
    }
  }
}