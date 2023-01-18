pipeline {
    agent any
    tools {
        maven "Maven 3.6.3"
    }
    stages {
        stage('Build Artifact'){
            steps{
                sh 'mvn clean package -DskipTests=true'
            }
        }
    }
}