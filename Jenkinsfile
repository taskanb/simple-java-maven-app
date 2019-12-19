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
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/*.xml'
                }
            }
        }
        }
     }

