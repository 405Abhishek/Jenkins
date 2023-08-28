pipeline{
	agent any
	environment{
		dockerHome = tool 'mydocker'
		mavenHome = tool 'mymaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Checkout') {
			steps{
			sh "mvn --version"
			sh "docker --version"
			echo "Build3"
	}
		}

		stage('Compile') {
			steps{
				sh "mvn clean complie"
			
	}
		}

	stage('Test') {
			steps{
				sh "mvn test"
			
	}
	}

	stage('Integration Test') {
			steps{
				sh "mvn failsafe:integration-test failsafe:verify"
			
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
