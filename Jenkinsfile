pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/rojakurva/java-tomcat-maven-example.git', branch: 'master')
      }
    }

    stage('build') {
      steps {
        bat 'mvn build'
      }
    }

  }
}