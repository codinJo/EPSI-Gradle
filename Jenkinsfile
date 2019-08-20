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
