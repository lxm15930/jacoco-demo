pipeline {
    agent any
    stages {
       stage('Build') {
            steps{
                bat "mvn clean package -Dmaven.test.skip=true"   
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
