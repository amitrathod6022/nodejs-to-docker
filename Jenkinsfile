node{
	
	def app
	stage('Clone Repository'){
		checkout scm
	}

	stage('Build Image'){
		app=docker.build('app');

	}

	
	stage('push image'){
		
		docker.withRegistry('https://208997411759.dkr.ecr.ap-south-1.amazonaws.com/app','ecr:ap-south-1:aws-amit-cred'){
		docker.image('app').push('latest')
		}
	}
}
