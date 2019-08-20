plugins {
  id "org.sonarqube" version "2.7"
}
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
  }
}
