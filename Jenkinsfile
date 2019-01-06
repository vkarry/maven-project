pipeline {
	agent any
	  tools {
            maven 'M3'
          }
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
