pipeline {
    agent any
    stages {
       stage('Build') {
            steps{
                bat "mvn clean jacoco:prepare-agent package -Dmaven.test.skip=true"   
            }
          }
		 
       stage('JacocoBuild') {
            steps{
                bat "mvn jacoco:report"
            }
          }		 
		  
	      stage('JacocoPublisher') {
            steps {
                 jacoco()
            }
		}	
		
    }      
}
