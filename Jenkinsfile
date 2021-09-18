pipeline {
    agent any
    stages {
      stage('checkout') {
           steps {
             
                git branch: 'master', url: 'https://github.com/lakshmi4025/DockerSampleApp.git'
             
          }
        }
 stages {
  stage('Docker Build and Tag') {
           steps {
              
                sh 'docker build -t apache2:latest .' 
                sh 'docker tag apache2 lakshmi1994/apache-lakshmi:v2'
                
               
          }
        }
     
  stage('Publish image to Docker Hub') {
          
            steps {
        withDockerRegistry([ credentialsId: "6f79449d-1bea-4769-b601-cfbbfc67381d", url: "https://hub.docker.com/repository/docker/lakshmi1994" ]) {
          sh  'docker push  lakshmi1994/apache-lakshmi:v2'
           
        }
                  
          }
        }
     
 }
