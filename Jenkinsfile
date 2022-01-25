pipeline {
  agent any
    
  tools {nodejs "NODEJS_14_LTS"}
    
  stages {       
    stage('Build') {
      steps {
        sh 'npm install'
         sh '<<Build Command>>'
      }
    }
  }
}
