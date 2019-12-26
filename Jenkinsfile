pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
				echo 'Build Starts!'
                dir ('simple-java-maven-app'){
				echo 'Build Ends!'
			}
          }
        }
        stage('Test') {
            steps {
                echo 'Test Starts!'
            }
		}
		
		post {
			always {
				junit 'target/surfire-reports/*.xml'
			}
		}
		    
 }
}
   

