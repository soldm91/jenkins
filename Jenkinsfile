pipeline {
  agent any
  stages {
    stage('Terraform Init') {
      steps {
        echo 'Executing terraform init'
        sh '''cd /home/ec2-user/terraform/newSubnet
terraform init'''
      }
    }
  }
}