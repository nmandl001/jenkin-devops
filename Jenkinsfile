pipeline {
	//agent { docker { image 'maven:3.6.3' } }
	agent any
	environment {
		dockerHome = tool "myDocker"
		mavenHome = tool "myMaven"
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
    stages {
        stage('build') {
            steps {
				echo "Build"
				sh 'mvn --version'
				sh 'docker version'
				echo "PATH - $PATH"
				echo "BUILD_NUMBER - $env.BUILD_NUMBER"
				echo "BUILD_ID - $env.BUILD_ID"
				echo "BUILD_TAG - $env.BUILD_TAG"
				echo "JOB_NAME - $env.JOB_NAME"
				echo "BUILD_URL - $env.BUILD_URL"
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

