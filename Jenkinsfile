pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
				echo 'Build Starts!'
                dir ('simple-java-maven-app'){
				bat 'mvn -B -DskipTests clean install'
				echo 'Build Ends!'
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
                bat './jenkins/scripts/deliver.sh'
            }
        }  
    }
 }
   

