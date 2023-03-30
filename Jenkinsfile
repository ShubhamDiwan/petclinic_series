pipeline {
    agent any
      
    stages {
        stage('Build and create docker image'){
            steps{
                sh "cd /root/.jenkins/workspace/Pipeline_Project/config-server"
                sh "pwd"
                sh "docker build -t config-server:${env.BUILD_ID} ."
            }
        }
    }
}
