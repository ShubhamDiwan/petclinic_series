pipeline {
    agent any
      
    stages {
        stage('Checkout code from git'){
            steps{
                git 'https://github.com/ShubhamDiwan/petclinic_series.git'
            }
        }
        
        stage('Build and create docker images'){
            steps{
                dir('config-server'){
                    sh "docker build -t config-server:${env.BUILD_ID} ."
                }
            }
            steps{
                dir('service-registry'){
                    sh "docker build -t service-registry:${env.BUILD_ID} ."
                }
            }
            steps{
                dir('hystrix-dashboard'){
                    sh "docker build -t hystrix-dashboard:${env.BUILD_ID} ."
                }
            }
            steps{
                dir('catalog-service'){
                    sh "docker build -t catalog-service:${env.BUILD_ID} ."
                }
            }
            steps{
                dir('inventory-service'){
                   sh "docker build -t inventory-service:${env.BUILD_ID} ."
                }
            }
            steps{
                dir('order-service'){
                    sh "docker build -t order-service:${env.BUILD_ID} ."
                }
            }
            steps{
                dir('shoppingcart-ui'){
                    sh "docker build -t shoppingcart-ui:${env.BUILD_ID} ."
                }
            }
            steps{
                dir('zipkin-server'){
                    sh "docker build -t zipkin-server:${env.BUILD_ID} ."
                }
            }
        }
    }
}
