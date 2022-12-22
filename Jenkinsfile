pipeline {
    agent any
    stages {
        stage('Delete the workspace'){
            steps{
                cleanWs()   
            }
        }    
        stage('Installing Java and Maven'){
            script {
                def maven_exists = fileExists '/usr/share/maven'
                if (mavenexists == true){
                    echo "skipping maven install - already exists"
                }
                else {
                    sh 'sudo apt update -y && apt upgrade -y'
                    sh 'sudo apt install -y wget tree unzip openjdk-11-jdk maven'
                }       
        }
        stage('Thrid Stage'){
            steps{
                echo "Thirs Stage"
            }
        }
    }
}
