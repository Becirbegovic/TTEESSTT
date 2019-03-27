#!groovy
pipeline {
    agent none
    environment {
        PATH = "C:\\devsbb\\cmder\\vendor\\git-for-windows\\bin;${env.PATH}"
    }

   stages {
      stage('Maven Install') {
         agent {
            docker {
               image 'maven:3.5.0'
            }
         }
         steps {
            sh 'mvn clean install'
         }
      }
   }
}
