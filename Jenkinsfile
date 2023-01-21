pipeline {
  agent any
  
  stages {
    stage ('Start nginx') {
      steps {
        sh 'sudo apt update -y'
        sh 'sudo apt install nginx -s'
      }
    }  
    stage ('index') {
      steps {
        sh """echo 'My first server on jenkins >> /var/www/html/index.html' """
      }          
    }
    stage ('start nginx') {
      steps {
        sh 'sudo systemctl start nginx'
      }
    }
    stage ('running processes') {
      steps {
        sh 'sudo stop'
      }
    }
  }
}
