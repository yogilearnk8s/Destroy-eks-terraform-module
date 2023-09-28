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
	   aws kms schedule-key-deletion --key-id arn:aws:kms:ap-south-1:014742839986:key/3ecef665-ad37-49f1-a5dc-910933f0fea2 
    --pending-window-in-days 7
      }
    }

  }
  
  
}
