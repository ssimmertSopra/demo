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
     		sh 'mvn deploy:deploy-file -DgroupId=com.example.innershift -DartifactId=demo -Dversion=0.0.1-SNAPSHOT -DgeneratePom=true -Dpackaging=jar -DrepositoryId=nexus -Durl=http://172.17.0.2:8081/repository/maven-snapshots/ -Dfile=target/demo-0.0.1-SNAPSHOT.jar'
  		}      
  	}
  }
}