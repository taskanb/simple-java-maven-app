pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir ('simple-java-maven-app'){
				sh 'mvn clean install test '
			}
          }
        }
        stage('Test') {
            steps {
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
