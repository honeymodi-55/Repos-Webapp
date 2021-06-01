pipeline {
    agent any 
    stages {
        stage ('Performing Maven Cleaning') {
            steps { sh 'mvn clean'}
        }
        stage ('Performing Maven Testing') {
            steps { sh 'mvn test'}
        }
        stage ('Building Maven Project') {
            steps { sh 'mvn package'}
        }
        stage ('Deployying the Maven Webapp into tomcat Server') {
            steps { sh 'sudo scp -i /home/ec2-user/keyfiles.pem /var/lib/jenkins/workspace/GitConnect_Repos-Webapp_main/target/artifactid.war ec2-user@172.31.3.159:/usr/share/tomcat/webapps'}
        }
    }
}