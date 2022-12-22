pipeline {
	agent any
	Stages {
		stage('Delete the Workspace'){
			steps {
				cleanWs()
			}
		}
		
		stage('Second Stage')
			steps {
				echo "Second stage"
			}
		}
		stage('Third stage'){
			steps{
				echo "Third Stage"
		}
	}
}
