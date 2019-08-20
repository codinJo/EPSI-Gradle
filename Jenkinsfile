pipeline {
  agent any
  stages {
    stage('jenkinsINIT') {
      steps {
        script {
          pipeline {
            agent any
            stages {
              stage('Compile') {
                steps {
                  sh './gradlew bootJar'
                }
              }
              stage('Unit Test') {
                steps {
                  sh './gradlew test'
                }
                post {
                  always {
                    junit '**/build/test-results.test/TEST-*.xml'
                  }
                }
              }
            }
          }
        }

      }
    }
  }
}