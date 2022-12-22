pipeline {
        agent any 
        stages {
            stage('Delete the workspace'){
                steps {
                    cleanWs()
                }
            }
            stage('Installing Java and Maven'){
                steps {
                    sh 'apt update && apt upgrade -y'
                    sh 'apt install -y wget tree unzip openjdk-11-jdk maven'
                }
            }
            stage('Third Stage'){
                steps {
                    echo "Third Stage"
                }
            }
        }
}
