pipeline {
    agent any
      
    stages {
        stage('Checkout code from git'){
                    steps{
                        git 'https://github.com/ShubhamDiwan/New_Docker_Project.git'
                    }
                }
      stage('Build Application'){
        steps{
          sh './run.sh start_all'
        }
      }
    }
}
