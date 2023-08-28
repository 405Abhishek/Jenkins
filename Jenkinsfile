pipeline{
	agent any
	stages{
		stage('build') {
			steps{
			echo "Build"
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
