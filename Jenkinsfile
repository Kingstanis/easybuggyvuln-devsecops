pipeline {
  agent any
  tools { 
        maven 'maven'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=devsecops -Dsonar.organization=cybersecurity-r-and-d -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=ab508d936ebd01404e03bd0c24c28c5f34587be7'
			}
        } 
  }
}
