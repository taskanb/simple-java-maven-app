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
                sh 'make'
				archieveartifacts artifacts: '**/target/*.jar', fingerprint: true
            }
            
           }
        }
      }
   

