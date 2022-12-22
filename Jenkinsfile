pipeline {
    agent any
    stages {
        stage('Delete the workspace') {
          steps {
            cleanWs()
          }
        }
        stage ('Second Stage'){
            steps {
                echo "Second Stage"
            }
        }
        stage ('Third Stage') {
            steps {
                echo "Third Stage"
            }
        }
        stage ('Installing Java and Maven') {
            steps {
                script {
                    def maven_exists = fileExists '/usr/share/maven'
                    if (maven_exists == true) {
                        echo "Skipping maven install - already exists"
                    }
                    else {
                        sh 'apt update && apt ugrade -y'
                        sh '    apt install -y weget tree unzip openjdk-11-jdk maven'
                    }
            }
        }
    }  
}
}
