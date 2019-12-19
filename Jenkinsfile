pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir ('simple-java-maven-app'){
			}
          }
        }
        stage('Compile') {
            steps {
                sh 'mvn clean install'
				
				}            
			}
        }
     }

