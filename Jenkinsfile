pipeline {
    agent any
      
    stages {
        stage('Build and create docker image'){
            steps{
                dir('config-server'){
                    sh "pwd"
                    sh "docker build -t config-server:${env.BUILD_ID} ."
                }    
            }
        }
    }
}
