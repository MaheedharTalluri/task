@Library('shlib')_
pipeline{
agent any
stages{
	stage('Create Job Jenkins'){
		steps{
			createjob("/var/lib/jenkins/workspace/${JOB_NAME}/dsltest.groovy","name")
		}
	}
	}
}