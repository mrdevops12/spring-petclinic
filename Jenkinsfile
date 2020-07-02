pipeline {
   agent any
   parameters {
       choice (
          choices: ['clean','compile','package','noneed']
          name: 'MVNTARGETS'
          description:'Please select the Mavne targets')
         }

   stages {
    stage("clone the remote repo"){
           steps {
               git branch: 'main', url: 'https://github.com/mrdevops12/spring-petclinic.git'
           }
       }
       stage("clean") {
          when {
             expresssion { params.MVNTARGETS == 'clean' }
          }     
          steps {
              sh "mvn clean"   
            } 
          }
        stage("compile") {
          when {
             expression { params.MVNTARGETS == 'compile' }
          }
          steps {
            sh "mvn compile"
            }  
          }
        stage("package") {
          when {
            expression { params.MVNTARGETS == 'package' }
          }
          steps {
            sh "mvn package"
          }
         }
}
}
