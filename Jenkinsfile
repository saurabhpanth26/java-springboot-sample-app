pipeline {
        agent any 
        stages {
            stage('Delete the workspace') {
                steps {
                    cleanWs()
                }
            }
            stage('Installing Java and Maven'){
                steps {
                    script {
                        def maven_exists = fileExists '/usr/share/maven'
                        if (maven_exists == true){
                        echo "Skipping maven install - already exists"
                        }
                        else {
                            sh 'apt update && apt upgrade -y'
                            sh 'apt install -y wget tree unzip openjdk-11-jdk maven'
                        }
                    }
                }
            }    
            stage('Third Stage'){
                steps {
                    echo "Third Stage"
                }
            }
        }
}   
