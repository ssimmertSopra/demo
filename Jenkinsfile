pipeline {
    agent any
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }

  stages {
    stage('compile') {
      steps {
        sh 'mvn clean install'
      }
    }
    }
}