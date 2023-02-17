pipeline {
	agent any
	
	stages {
		stage('Build') {
			steps {
				sh 'g++ ./pes1ug20cs112_task5.cpp -o ./pes1ug20cs112_task5'
				echo 'Build Stage Successful.'
				build job: 'PES1UG20CS112-1'
			}
		}
		stage('Test') {
			steps {
				sh './pes1ug20cs112_task5124'
				echo 'Test Stage Successful.'
			}
		}
		stage('Deploy') {
			steps {
				echo 'Deployment Successful.'
			}
		}
	}
	post {
		failure {
			echo 'Pipeline Failed.'
		}
	}
}
