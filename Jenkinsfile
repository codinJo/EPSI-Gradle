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
        bat './gradlew sonarqube -Dsonar.projectKey=codinJo_EPSI-Gradle -Dsonar.organization=codinjo -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=72b0834d0a710236f3190503203f2a029246c285'
      }
    }
  }
}