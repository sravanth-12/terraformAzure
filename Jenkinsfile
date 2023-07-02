pipeline {
    agent any
    tools {
       terraform 'Terraform'
       }
    stages {
        stage('Git checkout') {
           steps{
               git branch: 'main', credentialsId: 'sravanth', url: 'https://github.com/sravanth-12/terraformAzure.git'
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
