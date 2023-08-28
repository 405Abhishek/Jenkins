pipeline{
	//agent any
	agent { docker {image 'maven:3.6.3'}}
	stages{
		stage('build') {
			steps{
			sh "mvn --version"
			echo "Build2"
			echo "Build3"
	}
		}

		stage('test') {
			steps{
			echo "testt"
			echo "Test"
			echo "I test"
	}
		}
	}
	post{
		always{
			echo "I have done it"
		}
		success{
			echo "its a success"
		}
		failure{
			echo "we failed"
		}
	}
	
}
