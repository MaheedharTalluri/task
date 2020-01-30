@Library('shlib')_
pipeline{
agent any
stages{
	stage('Test Stage'){
		steps{
			def data = readJSON file: "${env.WORKSPACE}\\sample.json"
			data.ci.jobs.job.job_name
		}
	
	}




	stage('Create Job Jenkins'){
		steps{
			createjob("dsltest.groovy","name")
		}
	}
	stage('Trigger Build'){
	steps{
	jenkinsconnector("freestyle")
	}
	}
	stage('Jenkins collectors'){
	steps{
	buildstatus("freestyle",1)
	lastsuccessfulbuild("freestyle")	
		}
	}
	}
}