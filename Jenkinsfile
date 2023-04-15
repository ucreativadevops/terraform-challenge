pipeline{
    agent {
        label 'linux'
    }

    stages {
        stage('Terraform Format'){
            steps{
                echo 'Ejecutando terraform fmt'
            }
        }

        stage('Terraform Validate'){
            steps{
                echo 'Ejecutando terraform validate'
            }
        }

        stage('Terraform Plan'){
            steps{
                echo 'Ejecutando terraform plan'
            }
        }

        stage('Terraform Apply'){
            when { branch 'prod' }
            steps{
                echo 'Ejecutando terraform apply'
            }
        }

        stage('Terraform Destroy'){
            when { branch 'destroy-infra' }
            steps{
                sh '''
                    cd /terraform_location
                    terraform destroy
                '''
            }
        }
    }
}
