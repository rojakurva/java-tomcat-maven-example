pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/rojakurva/java-tomcat-maven-example.git', branch: 'master')
      }
    }

    stage('compile') {
      parallel {
        stage('compile') {
          steps {
            bat 'mvn clean compile'
          }
        }

        stage('install') {
          steps {
            bat 'mvn install'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        bat 'xcopy "C:\\Program Files (x86)\\Jenkins\\workspace\\java-tomcat-maven-example_master\\target" "C:\\Program Files\\Apache Software Foundation\\Tomcat 8.5\\webapps"'
      }
    }

  }
}