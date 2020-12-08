def var
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
       stage("deploy"){
         steps{
           sshagent(['deploy-user']) {
            sh 'scp -o StrictKeyHostChecking=no /var/lib/jenkins/workspace/jenkins_pipelines_master/target/WebAppCal-0.0.6.war centos@18.216.222.122:/home/centos/apache-tomcat-7.0.94/webapps'
           }
         }
       }
   }
 }  
        
