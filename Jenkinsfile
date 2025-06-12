pipeline {
  agent any
  tools { 
        maven 'maven'  
    }
   stages{
	   stage('Build Stage') {
		   steps {
			   sh 'mvn clean build'
			   }
		   }
	   stage('SonarAnalysis - SAST') {
		   steps {
			   sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=Kingstanis_devsecops -Dsonar.organization=cybersecurity-r-and-d -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=ab508d936ebd01404e03bd0c24c28c5f34587be7'
			   }
		   }
	   }
}
