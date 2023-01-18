pipeline {
  agent any
  
  stages {
    stage ('Start nginx') {
      steps {
        sh 'apt install nginx -y'
      }
    }  
    stage ('index') {
      steps {
        sh """echo 'My first server on jenkins >> /var/www/html/index.html' """
      }          
    }
    stage ('start nginx') {
      steps {
        sh 'systemctl start nginx'
      }
    }
  }
}
