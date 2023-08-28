pipeline{
	agent any
	environment{
		dockerHome = tool 'mydocker'
		mavenHome = tool 'mymaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('build') {
			steps{
			sh "mvn --version"
			sh "docker --version"
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
