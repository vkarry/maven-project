pipeline {
	agent any
	  tools {
            maven 'apache-maven-3.6.0'
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
