pipeline {
    agent any

    stages{
	stage('Create instance and install app'){
		steps{
			withAWS(credentials:'AWS Credentials'){
				sh 'cd ~/hello-terraform'
				sh 'terraform apply -auto-approve'
			}
		}
	}
    }
}
