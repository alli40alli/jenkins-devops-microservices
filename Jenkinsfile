properties([pipelineTriggers([githubPush()])])

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
			echo "Integration"
			}
		}
	}
}
