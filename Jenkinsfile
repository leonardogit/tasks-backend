pipeline {
    agent any
    stages {
        stage('Build Artifact'){
            steps{
            withMaven(maven : 'apache-maven-3.6.3'){
                bat 'mvn clean package -DskipTests=true'
                }
            }
        }
    }
}