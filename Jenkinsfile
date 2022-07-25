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
        stage("deploy-war"){
            steps{
                sshagent(['deploy_user']) {
                sh " scp -o StrictHostKeyChecking=no web/target/time-tracker-web-0.5.0-SNAPSHOT.war ec2-user@172.31.10.58:/home/ec2-user/apache-tomcat-9.0.65/webapps "
                 }
            }
        }
	}
} 
