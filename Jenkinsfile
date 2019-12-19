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
                dir('simple-java-maven-app/target')            }
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
