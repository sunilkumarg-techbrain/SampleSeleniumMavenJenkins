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
					 withMaven(maven: 'Maven 3') {
	                                  sh "mvn clean install"
		                              }  
						   } 
		           }
		       }
			 stage ('Allure Report Generation'){
	             steps {
				 
	                 script  {
					 withMaven(maven: 'Maven 3') {
	                                  sh "mvn allure:report"
		                              }  
		                   } 
		           }
		       }
			   			 
          }
}
