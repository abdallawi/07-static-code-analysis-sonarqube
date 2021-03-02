pipeline {
    agent any
    
    tools {
        maven 'my-maven-3' 
        
    }
    
    stages {
    	 
	//    stage ('Clone') {
    //         steps {
    //             git branch: 'master', url: "https://github.com/abdallawi/07-static-code-analysis-sonarqube.git"
    //         }
	//     }
	 
	  stage('Static Code Analysis '){
		  steps {
    		sh "mvn clean verify sonar:sonar   -Dsonar.projectName=07-static-code-analysis-sonarqube -Dsonar.projectKey=07-static-code-analysis-sonarqube -Dsonar.projectVersion=$BUILD_NUMBER";
		  }
	  }
    }
  }