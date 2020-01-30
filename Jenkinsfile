@Library('shlib')_
pipeline{
agent any
stages{
	stage('Test Stage'){
		steps{
			jtest()
		}
	
	}




	stage('Create Job Jenkins'){
		steps{
			createjob(dsl_filename,jenkins_jobname)
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