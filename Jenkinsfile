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

		stage('compile') {
			steps {
				def mvn_version = 'M3'
				withEnv( ["PATH+MAVEN=${tool mvn_version}/bin"] ) {
					sh 'mvn clean install'
				}
			}
		}
    }
}