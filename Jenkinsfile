//scripted pipeline approach


//declarative pipeline apprach
pipeline {
	
	//agent any
	agent { docker { image 'maven:3.8.1'} }
	stages{
		stage('Build')
		{
			steps{
				echo "Build"
			}
		}
		stage('Test')
		{
			steps{
				sh 'mvn --version'
				echo "Test"
			}
		}
		stage('Integration Test')
		{
			steps{
				echo "Integration Test"
			}
		}

	}
	post{
		always {
			echo 'I am awesome. I run always'
		}
		success { 
			echo 'I run when you are succesfull'
		}
		failure { 
			echo 'I run when you fail'
		}
	}
		
}
