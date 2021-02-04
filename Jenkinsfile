pipeline {

	agent any
//  agent { docker { image 'maven:3.6.3' } }
	environment {
		mavenHome = tool 'AliAMaven'
		dockerHome = tool 'AliADocker'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"	
	}
	stages {
		stage('Build') {
		steps {
			sh 'mvn --version'
			sh 'sudo docker version'
			echo "Build !"
			echo "$PATH"
			echo "BUILD_NUMBER"
			echo "$env.BUILD_NUMBER"
			echo "BUILD_NUMBER - $env.BUILD_NUMBER"
			}
		}
		stage('Test') {
		steps {
			echo "Test !!"
//			sh 'ls -a' 
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
