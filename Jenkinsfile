pipeline {
  
  agent any  
  
  stages {
    stage('checkout') {
      steps {
        checkout scm
  	    }
    	}
    
 
    stage('terraform destroy') {
      steps {
	    sh 'terraform init'
        sh 'terraform --version'
		sh 'terraform destroy --auto-approve'
      }
    }


  }
  
  
}