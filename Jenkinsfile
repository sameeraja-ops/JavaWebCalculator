def var
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
            sh "scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/jenkins_pipelines_master/target/ centos@18.216.222.122:~/"
           }
         }
       }
   }
 }  
        
