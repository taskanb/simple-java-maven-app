pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir ('simple-java-maven-app'){
			}
          }
        }
        stage('Test') {
            steps {
                echo 'Test'
            }
		
		stage('Deliver') {
			steps {
				sh './jenkins/scripts/deliver.sh'
			}
		}
            
           }
        }
      }
   

