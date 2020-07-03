pipeline {
   agent any
   stages {
    stage("clone the remote repo"){
           steps {
               git branch: 'main', url: 'https://github.com/mrdevops12/spring-petclinic.git'
           }
       }
       stage("clean") {
          steps {
              sh "mvn clean"
            }
          }
        stage("compile") {
          steps {
            sh "mvn compile"
            }
          }
        stage("package") {
          steps {
            sh "mvn package"
          }
         }
		stage("Reading values from pom"){
		 steps {
		   script{
		     def pom = readMavenPom file: 'pom.xml'
			 projectName = pom.getName()
			 sh "echo ${pom.version}"
			 sh "echo ${pom.parent.version}"
			 sh "echo ${pom.name}"
			 }
		}
	}	 
}
}

