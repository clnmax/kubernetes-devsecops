pipeline {
  agent any

  stages {
      stage('Build Artifact') {
            steps {
              sh "mvn clean package -DskipTests=true"
              archive 'target/*.jar'
            }
        } 

       stage('check docker version') {
            steps {
              sh "docker --version" //afficher la version docker
            }
        }  
         stage('check maven version') {
            steps {
              sh "mvn --version" ///
            }
        }
    }
}
