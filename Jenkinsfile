pipeline{
    agent any
    stages{
        stage("Gitpull"){
            steps{
                git credentialsId: 'Github', url: 'https://github.com/kishoremc/example-java-pom.git'
            }
        }
        stage("Maven-Job"){
            steps{
                sh " mvn clean install"
            }
        }
    }
} 
