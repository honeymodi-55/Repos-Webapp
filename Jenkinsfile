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
    }
}