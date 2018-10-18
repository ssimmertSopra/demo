pipeline {
  agent any
  tools {
    mvn 'M3'
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install'
      }
    }
  }
}