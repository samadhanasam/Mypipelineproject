pipeline {
  agent any
  
  tools {
  maven "MAVEN_HOME"
  }
  
  stages {
   stage('Compile') {
        steps {
           echo "mvn clean compile"
             }
            }
   stage('Test') {
        steps {
           echo "mvn clean test"
             }
            }
   stage('Deploy') {
        steps {
           echo "mvn clean install"
             }
            }
       }
       }
  
  
      

  
