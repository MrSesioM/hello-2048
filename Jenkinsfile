pipeline {
    agent any

    stages{
	stage('Create instance and install app'){
		step{
			withAWS(credentials:'AWS Credentials'){
				sh 'terraform apply'
			}
		}
	}
    }
}
