pipeline {
    agent any
    
    options {
        timestamps()
        ansiColor('xterm')
    }

    stages {
        stage('Docker-login') {
            steps {
                withCredentials([string(credentialsId: 'docker-login', variable: 'CR_PAT')]) {
                    sh 'echo $CR_PAT | docker login ghcr.io -u mrsesiom --password-stdin'
                    
                }
            }
        }
	stage('Build') {
            steps {
                sh 'docker build -t ghcr.io/MrSesioM/2048:latest .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker-compose up -d'
            }
        }
    
    }
}
