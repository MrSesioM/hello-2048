pipeline {
    agent any

    stages{
	stage('Create instance and install app'){
		steps{
			withAWS(credentials:'AWS Credentials'){
				sh 'terraform apply'
			}
		}
	}
    }
}
