pipeline {
    agent any
      
    stages {
        stage('Checkout code from git'){
            steps{
                git 'https://github.com/ShubhamDiwan/petclinic_series.git'
            }
        }
        
        stage('Build and create config-server docker images'){
            steps{
                dir('config-server'){
                    sh "docker build -t config-server:${env.BUILD_ID} ."
                }
            }
        }
        stage('Build and create service-registry docker images'){
            steps{
                dir('service-registry'){
                    sh "docker build -t service-registry:${env.BUILD_ID} ."
                }
            }
        }
        stage('Build and create hystrix-dashboard docker images'){
            steps{
                dir('hystrix-dashboard'){
                    sh "docker build -t hystrix-dashboard:${env.BUILD_ID} ."
                }
            }
        }
        stage('Build and create catalog-service docker images'){
            steps{
                dir('catalog-service'){
                    sh "docker build -t catalog-service:${env.BUILD_ID} ."
                }
            }
        }
        stage('Build and create inventory-service docker images'){
            steps{
                dir('inventory-service'){
                   sh "docker build -t inventory-service:${env.BUILD_ID} ."
                }
            }
        }
        stage('Build and create order-service docker images'){
            steps{
                dir('order-service'){
                    sh "docker build -t order-service:${env.BUILD_ID} ."
                }
            }
        }   
        stage('Build and create shoppingcart-ui docker images'){
            steps{
                dir('shoppingcart-ui'){
                    sh "docker build -t shoppingcart-ui:${env.BUILD_ID} ."
                }
            }
        }
        stage('Build and create zipkin-server docker images'){
            steps{
                dir('zipkin-server'){
                    sh "docker build -t zipkin-server:${env.BUILD_ID} ."
                }
            }
        }
    }
}
