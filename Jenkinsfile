pipeline{
    agent any
    stages{
        stage("Gitpull"){
            steps{
                git credentialsId: 'Github', url: 'https://github.com/kishoremc/time-tracker.git'
            }
        }
        stage("Maven-Job"){
            steps{
                sh " mvn clean install"
            }
        }
    }
} 
