pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir ('simple-java-maven-app'){
			}
          }
        }
        stage('Archive') {
            steps {
                dir('simple-java-maven-app'){
				archieve '*.jar'
				}            
			}
        }
     }
 }

