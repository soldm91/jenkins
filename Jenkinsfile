pipeline {
  agent any
  stages {
    stage('Create subnet') {
      steps {
        echo 'creating subnet'
        sh '''id
cp -f /home/ec2-user/terraform/newSubnet/newSubnet.tf newSubnet.tf'''
        sh 'terraform init'
        sh 'terraform plan'
        sh 'terraform apply'
      }
    }
    stage('Sleep 5 Minutes') {
      steps {
        echo 'Sleeping'
        sleep(time: 5, unit: 'MINUTES')
        echo 'done sleeping'
      }
    }
    stage('Destroy') {
      steps {
        echo 'destroying'
        sh 'terraform -force destroy || true'
      }
    }
  }
}