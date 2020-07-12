pipeline {
   agent {
        label "master"
         }
   stages {
	         stage ('GIT checkout'){
	             steps {
	                 script  {
		                   git "https://github.com/sunilkumarg-techbrain/SampleSeleniumMavenJenkins"
		                   } 
		           }
		       }
			 stage ('Maven Test Execution'){
	             steps {
	                 script  {
	                       sh "mvn clean install"
		                   } 
		           }
		       }
			 stage ('Allure Report Generation'){
	             steps {
	                 script  {
		                   sh "mvn allure:report"

		                   } 
		           }
		       }
			   			 
}
