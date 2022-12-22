pipeline {
    agent any
    stages {
        stage('Delete the workspace') {
          steps{
            cleanWs()
          }
        }
        stage ('Second Stage')
            steps {
                echo "Second Stage"
            }
        }
        stage ('Thirs Stage')
            steps {
                echo "Third Stage"
            }
        }
    }  
}
