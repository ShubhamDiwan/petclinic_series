pipeline {
    agent any
      
    stages {
        stage('Checkout code from git'){
            steps{
                git 'https://github.com/ShubhamDiwan/petclinic_series.git'
            }
        }
        stage('Build Application'){
            steps{
                sh './mvnw clean package -DskipTests=true'
            }
        }
        stage('Build and create docker image'){
            steps{
                sh "cd config-server"
                sh "docker build . -t config-server:${env.BUILD_ID}"
            }
        }
    }
}
