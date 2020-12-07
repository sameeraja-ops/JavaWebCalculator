pipeline{
  agent any
  environment{
    SERVER_CREDENTIALS = credentials('server-credentials')
    stages {
       stage("build"){
         steps{
            withcredentials([
               usernamePassword((credentialsId : 'server-credentials', usernameVariable : Username, passwordVariable : Password))
              ])
           {
           sh "mvn install"
           sh "mvn clean package"
          }
         }
        }
       stage("test"){
         steps{
           echo "Testing the application"
           }
         }
   }
 }  
        
