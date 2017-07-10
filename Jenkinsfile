pipeline {
  agent any
  stages {
    stage('Create subnet') {
      steps {
        echo 'creating subnet'
        sh 'cp -f /home/ec2-user/terraform/newSubnet/newSubnet.tf'
        sh 'terraform init'
        sh 'terraform plan'
        sh 'terraform apply'
      }
    }
  }
}