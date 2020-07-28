pipeline {
    agent any
    stages {
       stage('Build') {
            steps{
                bat "mvn clean package"   
            }
          }
		 
       stage('JacocoBuild') {
            steps{
                bat "mvn jacoco:prepare-agent jacoco:report"
            }
          }		 
		  
	      stage('JacocoPublisher') {
            steps {
                 jacoco()
            }
		}	
		
    }      
}
