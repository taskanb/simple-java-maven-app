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
		  
		post {
		success {
			archieveArtifacts 'target/*.hpi, target/*.jpi'
			}
	}
}
	
        stage('Test') {
            steps {
                echo 'Test Starts!'
            }
		post {
			always {
				junit 'target/surefire-reports/*.xml'
		}
	}
}

		stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
            }
        }  
    }
 }
   

