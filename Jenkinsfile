pipeline{
  agent any
  tools{
   maven 'Maven'
   }
    stages {
       stage("build"){
         steps{
           sh "mvn install"
           sh "mvn clean package"
          }
        }
       stage("test"){
         steps{
           echo "Testing the application"
           }
         }
   }
 }  
        
