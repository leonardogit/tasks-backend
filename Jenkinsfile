pipeline {
    agent any
    stages {
        stage('Build Artifact'){
            steps{
                bat 'mvn clean package -DskipTest=true'
            }
        }
    }
}