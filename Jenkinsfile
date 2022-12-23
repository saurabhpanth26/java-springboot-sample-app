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
            stage('Download Java Code'){
                steps {
                    git credentialsId: 'git-repo-creds', url: 'git@github.com:saurabhpanth26/java-springboot-sample-app.git'
                }
            }
            stage('Compiling and Running Test Cases') {
                steps {
                    sh 'mvn clean'
                    sh 'mvn compile'
                    sh 'mvn test'
                }
            }
            stage('Creating Package') {
                steps {
                    sh 'mvn package'
                }
            } 
        }
}
