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
				sh 'mvn test'
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
   

