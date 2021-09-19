pipeline {
    agent {Dockerfile true}
    stages {
      stage('checkout') {
           steps {
             
                git branch: 'master', url: 'https://github.com/lakshmi4025/DockerSampleApp.git'
             
          }
        }
  stage('Docker Build and Tag') {
           steps {
              
                sh 'docker build -t apache2:latest .' 
                sh 'docker tag apache2 lakshmi1994/apache-lakshmi:v2'
                
               
          }
        }
 }
        
     
 
           
        
                  
          
     
 
    
    
     
 
        
