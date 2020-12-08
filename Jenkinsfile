
pipeline{
  agent any
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
            sh "scp /var/lib/jenkins/workspace/jenkins_pipelines_master/target/WebAppCal-0.0.6.war centos@18.216.222.122:~/"
           }
         }
       }
   }
 }  
        
