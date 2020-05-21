pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/rojakurva/java-tomcat-maven-example.git', branch: 'master')
      }
    }

    stage('compile') {
      steps {
        bat 'mvn clean compile'
      }
    }

  }
}