pipeline {
    agent any
    stages ('Download Java Code') {
        steps{
        git credentialsId: 'git-repo-creds', url: 'git@github.com:saurabhpanth26/java-springboot-sample-app.git'
        }
    }
 }
