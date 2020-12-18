pipeline {
  agent any
  
  tools {
  maven "MAVEN_HOME"
  }
  
  stages {
   stage('Build') {
        steps {
           git 'https://github.com/samadhanasam/Mypipelineproject.git'
           echo 'mvn -Dmaven.test.failure.ignore=true clean compile'
             }
            }
   stage('Test') {
        steps {
           git 'https://github.com/samadhanasam/Mypipelineproject.git'
           echo 'mvn -Dmaven.test.failure.ignore=true clean test'
             }
            }
   stage('Deploy') {
        steps {
           git 'https://github.com/samadhanasam/Mypipelineproject.git'
           echo 'mvn -Dmaven.test.failure.ignore=true clean install'
             }
            }
       }
       }
  
