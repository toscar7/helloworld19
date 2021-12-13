pipeline {
   agent any 
   tools {
      maven 'M2_HOME'
   }
   environment {
    registry = "toscar7/devops-docker"
    registryCredential = 'dockerhub'
   }
   stages {
     stage('build'){
       steps {
        sh 'mvn clean'
        sh 'mvn install'
        sh 'mvn package'
      }
    }
    stage('test'){
      steps {
       echo "test step"
       sh 'mvn test'
      }
    }
    stage('deploy'){
      steps {
       echo "deploy step"
       sleep 10
      }
    }
    stage('docker'){
      steps {
       echo "image steps"
       sleep 10
      }
     }
   }
}
