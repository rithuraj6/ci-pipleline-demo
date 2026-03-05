pipeline {
	agent any
	tools {
		maven 'Maven'
	}
	stages{
		stage('Checkout Code') {
			steps {
				git 'https://github.com/rithuraj6/ci-pipleline-demo.git'
			}
		}
		

		stage('Build') {
			steps {
				sh 'mvn clean compile'
			}
		}
		
		stage('Unit Test') {
			steps {
				sh 'mvn test'
			}
		}

		stage('Sonar Analysis') {
			steps {
				sh 'mvn sonar:sonar'
			}
		}
    	}
}
