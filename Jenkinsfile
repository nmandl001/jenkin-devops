pipeline {
	agent { docker { image 'maven:3.6.3' } }
    stages {
        stage('build') {
            steps {
				echo "Build"
				sh 'mvn --version'
            }
        }
		stage('Test') {
            steps {
				echo "Test"
            }
        }
		stage('Integration Test') {
            steps {
				echo "Integration Test"
            }
        }
    } 
	post {
		always{
			echo "I am awesome. I always run"
		}
		success {
			echo "I am awesome. Success"
		}
		failure {
			echo "I am awesome. Failure"
		}
	}
}

