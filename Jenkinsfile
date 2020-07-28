pipeline {
    agent any
    stages {
       stage('Build') {
            steps{
               bat "mvn org.jacoco:jacoco-maven-plugin:prepare-agent -f pom.xml clean test -Dautoconfig.skip=true -Dmaven.test.skip=false -Dmaven.test.failure.ignore=true" 
			  junit '**/target/surefire-reports/*.xml'
			//code coverage.LineCoverage>60%.
			jacoco changeBuildStatus: true, maximumLineCoverage:"60"			   
            }
          }
		
    }      
}
