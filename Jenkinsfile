pipeline {
    agent any
    stages {
        stage('Build Backend'){
            steps{
                bat 'mvn clean package -DskipTest=true'
            }
        }
        stage('Unit Tests'){
             steps{
                 bat 'mvn test'
             }
         }
        stage('Sonar Analysis'){
             environment {
                scannerHome = tool 'SONAR_SCANNER'
             }
             steps{
                 withSonarQubeEnv('SONAR_LOCAL'){
                  bat "${scannerHome}/bin/sonar-scanner -e -Dsonar.projectKey=DeployBack -Dsonar.host.url=http://localhost:9000 -Dsonar.login=e8fdac5cfeaf74953c6924f97c6a4e12b86f0058 -Dsonar.java.binaries=target -Dsonar.coverage.exclusions=**/.mvn/**,**/src/test/**,**/model/**,**/Application.java/**"
                 }
             }
         }
    }
}
