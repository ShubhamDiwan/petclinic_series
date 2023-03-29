pipeline {
    agent any
      
    stages {
        stage('Build and create docker image'){
            steps{
                sh "cd config-server"
                sh "docker build -t config-server:${env.BUILD_ID} ."
            }
        }
    }
}
