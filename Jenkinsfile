pipeline {
   agent {
        label "master"
         }

   stages {
	         stage ('GIT checkout'){
		        git "https://github.com/sunilkumarg-techbrain/SampleSeleniumMavenJenkins"
		     }
	         stage ('Maven Test Execution'){
	            sh "mvn clean install"
             }   
	         stage ('Allure Report Generation'){
	            sh "mvn allure:report"
		     }
          }
}
