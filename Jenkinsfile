pipeline {
   agent any
   stages {
       stage("repo clone"){
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

   }
}
