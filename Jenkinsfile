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
				sh "mvn clean compile"
			
	}
		}

	stage('Test') {
			steps{
				echo "TEst"
			
	}
	}

	stage('Integration Test') {
			steps{
				echo "Integration test"
			
	}
	
	stage('Package') {
			steps{
				sh "mvn package -DskipTests"
			
	}
		}

		stage('Build Docker Image') {
			steps{
				//"docker build -t in28min/currency-exchange-devops:$env.BUILD_TAG"
				script{
					dockerImage = docker.build("405ansh/currency-devops-demo:${env.BUILD_TAG}")
				}
			
	}
		}

		stage('Push Docker Image') {
			steps{
				script{
					docker.withRegistry('','dockerhub'){

					
					dockerImage.push();
					dockerImage.push('latest')
					}
				}
				
			
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
}
