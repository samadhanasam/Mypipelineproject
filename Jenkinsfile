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
           echo 'mvn clean install'
             }
     post {
              success {
                  deploy adapters: [tomcat8(credentialsId: '3420f31c-aa74-4b6d-9433-92662608e8be', path: '', url: 'http://localhost:8080/')], contextPath: 'rps', war: '**/assets/build/*.war'
              }

          }
            }
       }
       }
  
