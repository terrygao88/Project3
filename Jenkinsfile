pipeline {
	agent any
	tools {
    	maven 'local-mvn'
	}
	stages {
    	stage("Checkout") {   
        	steps {               	 
            	git branch: 'main',  url: 'https://github.com/terrygao88/Project3.git'          	 
           	 
        	}    
    	}
    	stage('Build') {
        	steps {
        	sh "mvn compile"  	 
        	}
    	}
   	 
    	stage("Unit test") {          	 
        	steps {  	 
            	sh "mvn test"          	 
       	    }
        }
        stage ('Package') {
                steps {
                build job: 'project3'
            }
        }		
    }
}
