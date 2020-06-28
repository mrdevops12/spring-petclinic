pipeline {
    agent any
    stages {
        stage('Source'){
            steps {
                git 'https://github.com/mrdevops12/spring-petclinic.git' 
            }
        }
        stage('Package'){
            steps {
                sh 'mvn package'
            }
        }
    }
}
