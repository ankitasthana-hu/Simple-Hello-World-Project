pipeline {
  agent any
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
  environment {
    maven = 'M2_HOME'
    JDK = 'JAVA_HOME'
  }
}