pipeline {
	agent any
	stages {
		stage('Clone repository') {
      			checkout scm
    		}
		stage('Create Image') {
			agent {
				dockerfile: true
			}
			steps {
				sh 'docker login -u nvierass -p Grupo4Mingeso'
				sh 'docker build . -t nvierass/mingeso:frontend-mingesog4'
				sh 'docker push -t nvierass/mingeso:frontend-mingesog4'
			}
		}
	}
}
