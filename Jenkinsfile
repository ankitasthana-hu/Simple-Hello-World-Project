pipeline {
  agent any
  
    tools {
      maven 'M2_HOME'
                 jdk 'JAVA_HOME'
    }
    
  
  stages {
    stage('Build') {
      steps {
        echo 'Hello World GIT Repo'
      }
    }

    stage('Build 1 - App') {
      steps {
        sh 'mvn clean install -DskipTests'
      }
    }

  }
}
