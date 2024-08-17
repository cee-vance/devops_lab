pipeline{
	agent any
	 tools { go 'go 1.19' }

	environment {
		ENV = "${env.BRANCH_NAME == 'master' ? 'PROD': 'DEV'}"
	}
	stages{
	stage('Build') {
		steps{
			bat 'scripts\\build.sh' // run the build.sh asset
		}
	
	}
	stage('Test'){
		steps{
			bat 'scripts\\test.sh' // run test.sh asset
		}
	}
	}

}
