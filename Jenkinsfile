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
    
     stage('terraform plan destroy') {
      steps {
	//      sh 'terraform init'
	//    sh 'terraform plan -destroy'
      
    sh 'terraform state list'
      sh 'terraform state rm module.eks_cluster_creation.kubernetes_config_map.aws_auth[0]'
      }
    }

//    stage('terraform destroy') {
//      steps {
//	      sh 'terraform init'
//	    sh 'terraform destroy --auto-approve'

//      }
//    }

  }
  
  
}
