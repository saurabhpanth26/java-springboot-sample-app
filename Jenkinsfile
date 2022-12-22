pipeline {
    agent any
    stages ('Installing Java and Maven') {
            steps {
                script {
                    def maven_exists = fileExists '/usr/share/maven'
                    if (maven_exists == true) {
                        echo "skipping maven install - already exists"
                    }         
                    else {
                        sh 'apt update && sudo apt-get upgrade -y'
                        sh 'apt install -y wget tree unzip openjdk-11-jdk maven'
                    }
            } 
    }
 }
