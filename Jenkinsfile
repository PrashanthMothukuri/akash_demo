pipeline {
	agent any
	stages {
		stage('Git-Checkout') {
			steps {
					echo "checking out from Git repo !!";
					git branch: 'main', credentialsId: '3186a2d7-901a-4ffe-9921-fdc969b60742', url: 'https://github.com/PrashanthMothukuri/akash_demo.git'
			}
		}
		
		stage('Deploy') {
			steps {
					echo "Building the checked out project ";
					sh 'docker-compose -f deploy.yaml up'
			}
		}
		
		
		
		
	}
}
