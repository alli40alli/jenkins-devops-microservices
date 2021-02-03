pipeline {

	agent any
	
	stages {
		stage('Build') {
		steps {
			echo "Build"
			}
		}
		stage('Test') {
		steps {
			echo "Test"
			}
		}
		stage('Integration') {
		steps {
			echo "Integrations"
			}
		}
	}
	post {
		always {
			echo "I always run"
		}
		success {
			echo "I run once the build succeed"
		}
		failure {
			echo "I run when the build fail"
		}
	}
}
