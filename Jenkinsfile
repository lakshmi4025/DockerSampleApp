pipeline {
    agent {
        Dockerfile true
    }
    stages {
      stage('checkout') {
           steps {
             
                git branch: 'master', url: 'https://github.com/lakshmi4025/DockerSampleApp.git'
             
          }
        }
     
  stage('Docker Build and Tag') {
           steps {
              
                sh 'docker build -t apache2 .' 
           }
  
  }
        
    }   
}
               
       
        
 
        
     
 
           
        
                  
          
     
 
    
    
     
 
        
