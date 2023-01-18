pipeline {
    agent any
    stages {
        stage('Build Back-End'){
            steps{
                sh 'mvn clean package -DskipTests=true'
            }
        }
    }
}