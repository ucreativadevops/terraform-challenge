pipeline{
    agent {
        label 'linux'
    }

    stages {
        stage('Terraform Format'){
            steps{
                sh 'Ejecutando terraform fmt'
            }
        }

        stage('Terraform Validate'){
            steps{
                sh 'Ejecutando terraform validate'
            }
        }

        stage('Terraform Plan'){
            steps{
                sh 'Ejecutando terraform plan'
            }
        }

        stage('Terraform Apply'){
            when { branch 'prod' }
            steps{
                sh 'Ejecutando terraform apply'
            }
        }
    }
}
