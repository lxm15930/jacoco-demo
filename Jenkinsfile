pipeline {
    agent any
    stages {
       stage('Build') {
            steps{
                withMaven(maven: 'maven'){
                      bat "mvn clean package -Dmaven.test.skip=true"
                }
            }
          }
		 
       stage('JacocoBuild') {
            steps{
                withMaven(maven: 'maven'){
                      bat "mvn jacoco:prepare-agent jacoco:report"
                }
            }
          }		 
		  
	      stage('JacocoPublisher') {
            steps {
                 jacoco()
            }
		}	
		
    }
	

        
}
