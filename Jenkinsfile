pipeline {
    agent any
 stages {
  stage('Docker Build and Tag') {
           steps {
              
                sh 'docker build -t apache2:latest .' 
                sh 'docker tag apache2 lakshmi1994/apache-lakshmi:v2'
                
               
          }
        }
     
  stage('Publish image to Docker Hub') {
          
            steps {
        withDockerRegistry([ credentialsId: "dockerHub", url: "https://hub.docker.com/repository/docker/lakshmi1994" ]) {
          sh  'docker push  lakshmi1994/apache-lakshmi:v2'
           
        }
                  
          }
        }
     
 }
