pipeline {
    agent any
      
    stages {
        stage('Checkout code from git'){
                    steps{
                        git 'https://github.com/ShubhamDiwan/Springboot.git'
                    }
                }
      stage('Build Application'){
        steps{
          sh './run.sh start_all'
        }
      }
    }
}
