@Library('shlib')_
pipeline{
agent any
stages{
	stage('Test Stage'){
		steps{
			jtest("sample.json")
			
		}
	
	}




	stage('Create Job Jenkins'){
		steps{
			createjob(${DSL_NAME},${JENKINS_NAME})
			
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