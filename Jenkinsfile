pipeline {
   agent any
   stages {
       stage("git cline"){
           steps {
               git branch: 'main', url: 'https://github.com/mrdevops12/spring-petclinic.git'
           }
       }
       stage("Package") {
          steps {
              sh "mvn package"
          } 
       }

   }
}
