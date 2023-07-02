pipeline {
    agent any
    tools {
       terraform 'Terraform'
       }
    stages {
        stage('Git checkout') {
           steps{
               git branch: 'main', credentialsId: 'bd47ee0c-8b80-466d-b814-08d8a1b0909a', url: 'https://github.com/sravanth-12/terraformAzure.git'
            }
        }
        stage('terraform Init') {
            steps{
                sh 'terraform init'
            }
        }
        stage('terraform apply') {
            steps{
                sh 'terraform apply -auto-approve'
            }
        }
    }

    
}
