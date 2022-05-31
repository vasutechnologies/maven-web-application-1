node
{
 def mavenHome = tool name: "maven3.8.5"
 properties([buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')), pipelineTriggers([pollSCM('* * * * *')])])
 stage('CheckoutCode')
  {
      git branch: 'development', credentialsId: 'ba5d4ca8-36ba-445a-bb02-6750ff434875',
      url: 'https://github.com/vasutechnologies/maven-web-application-1'
  } 
 stage('Build')
  {
     sh "${mavenHome}/bin/mvn clean package" 
  }
  /*
 stage("ExecuteSonarQubeReport")
 {
      sh "${mavenHome}/bin/mvn sonar:sonar"
 }
 stage('generatingpackage')
 { 
     sh "${mavenHome}/bin/mvn deploy"
 }  
 stage('Deployment into tomcat')
 {
     sshagent(['5b8acabd-9f6b-4588-9ef2-97fecae0e660'])
    {
        sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ec2-user@3.110.107.125:/opt/apache-tomcat-9.0.63/webapps"
    } 
 }
 stage('Sending email')
 {
 mail bcc: '', body: '''Buildover

Regards,
sunraj22
vasuautomobiles.''', cc: 'sunrajsur@gmail.com', from: '', replyTo: '', subject: 'Buildover', to: 'vasunaruboina21@gmail.com'
 }
 */
} 
