pipeline {
	agent any
	  stages {
	    stage ('Build') {
	      steps {
	        sh 'mvn clean packge'
	      }

	      post {
	        success {
	          echo "Archiving..."
	          archiveArtifacts artifacts: '**/target/*.war'
	        }
	      }
	    }
	  }
}
