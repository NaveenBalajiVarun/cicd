#!/bin/bash
pipeline {
  agent any
    
  tools {nodejs "NodeJS"}
  stages {   
    stage('Git') {
      steps {
         git 'https://github.com/Manoj-ramanathan/cicd.git'
      }
    }
    stage('Build') {
      steps {
       bat 'npm install'
        
        bat 'npm run build'
      }
    }
    //stage('deploy') {
      //steps {
        //sshagent(['deploy']) {
         //sh 'scp -r  /C:/Windows/System32/config/systemprofile/AppData/Local/Jenkins/.jenkins/workspace/cicdpipeline/build/* ec2-user@54.145.136.12:8080/opt/apache-tomcat-8.5.66/webapps/'
        //}
     // }
    //}
  }
}
