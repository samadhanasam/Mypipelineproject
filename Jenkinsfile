pipeline {
  agent any
  
  tools {
  maven "MAVEN_HOME"
  }
  
  stages {
   stage('Build') {
        steps {
           echo 'mvn clean compile'
             }
            }
   stage('Test') {
        steps {
           echo 'mvn clean test'
             }
            }
   stage('Deploy') {
        steps {
           echo 'mvn clean install'
             }
            }
       }
       }
  

stages {
      stage('Build') {
         steps {
            // Get some code from a GitHub repository 
            git 'https://github.com/jglick/simple-maven-project-with-tests.git'
            sh "mvn -Dmaven.test.failure.ignore=true clean compile"
         }
         }
      stage("Test") {
          steps {
            git 'https://github.com/jglick/simple-maven-project-with-tests.git'  
            sh "mvn -Dmaven.test.failure.ignore=true clean test"
            
          }

      }
      stage("Deploy") {
          steps {
            git 'https://github.com/jglick/simple-maven-project-with-tests.git'  
            sh "mvn -Dmaven.test.failure.ignore=true clean install"
            
          }
  
      

  
