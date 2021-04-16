pipeline {
  agent {
    docker {
      image 'maven'
      args 'M2_HOME'
    }

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