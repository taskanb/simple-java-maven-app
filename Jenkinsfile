pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir ('simple-java-maven-app'){
				sh 'mvn -B -DskipTests clean package'
			}
          }
        }
        stage('Test') {
            steps {
                echo 'Test'
            }
		}
		    
    }
 }
   

