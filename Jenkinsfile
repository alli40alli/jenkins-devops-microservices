pipeline {

	agent any
// for docker agents   agent { docker { image 'maven:3.6.3' } }
	stages {
		stage('Build') {
		steps {
// for docker agents			sh 'mvn --version'
			echo "Build !"
			}
		}
		stage('Test') {
		steps {
			echo "Test !"
// for docker agents			sh 'ls -a' 
			}
		}
		stage('Integration') {
		steps {
			echo "Integration !"
			}
		}
	}
	post {
		always {
			echo "I always run !"
		}
		success {
			echo "I run once the build succeed"
		}
		failure {
			echo "I run when the build fail"
		}
	}
}
