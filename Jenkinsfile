pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        bat './gradlew bootJar'
      }
    }
    stage('Test') {
      steps {
        bat './gradlew test'
      }
    }
    stage('SonarQube analysis') {
      steps {
        bat './gradlew sonarqube'
      }
    }
  }
}