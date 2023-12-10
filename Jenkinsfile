pipeline{
	agent { any { image 'golang:1.21.5-alpine3.19' }}
	// tools { go 'go 1.19' }

	environment {
		ENV = "${env.BRANCH_NAME == 'master' ? 'PROD': 'DEV'}"
	}
	stages{
	stage('Build') {
		steps{
			bat 'bash scripts/build.sh' // run the build.sh asset
		}
	
	}
	stage('Test'){
		steps{
			bat 'bash scripts/test.sh' // run test.sh asset
		}
	}
	}

}
