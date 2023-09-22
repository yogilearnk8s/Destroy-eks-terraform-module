pipeline {
  
  agent any  
	  options {
      timeout(time: 1, unit: 'HOURS') 
  }
  
  stages {
    stage('checkout') {
      steps {
        checkout scm
  	    }
    	}
    
 
    stage('terraform plan') {
      steps {
	      sh 'terraform init'
	    sh 'terraform destroy --auto-approve'
      }
    }

  }
  
  
}
