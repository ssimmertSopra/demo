pipeline {
  agent any
  tools {
    maven 'mvn'
  }
  stages {
    stage('Build') {
      	steps {
        	sh 'mvn clean install'
      	}
    }
    stage('Deploy') {
      	steps {
     		sh 'mvn deploy:deploy-file -DgroupId=com.somecompany -DartifactId=project -Dversion=1.0.0 -DgeneratePom=true -Dpackaging=jar -DrepositoryId=nexus -Durl=http://localhost:8081/repository/maven-releases -Dfile=target/demo-1.0.0.jar'
  		}      
  	}
  }
}