pipeline {
    agent any
    stages {
        stage('Build Artifact'){
            steps{
                bat 'mvn clean package -DskipTest=true'
            }
        }
        stage('Unit Tests'){
             steps{
                 bat 'mvn test'
             }
         }
    }
}