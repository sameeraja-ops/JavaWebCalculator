pipeline{
  agent any
  //environment{
    //SERVER_CREDENTIALS = credentials('server-credentials')
  //}
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
        
