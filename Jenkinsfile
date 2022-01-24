pipeline {
	agent {
    label 'docker' 
  }
	stages {
		stage('Build') {
      agent {
        docker {
          // Set both label and image
          label 'docker'
          image 'maven:3-alpine'
        }
      }
	  steps {
        // Steps run in maven:3-alpine docker container on docker slave
        sh 'mvn --version'
      }
	}
		stage("Test") {
			steps {
				
				echo "Test"
				
			}
		}
		stage("Integration Test") {
			steps {
				
				echo "Integration Test"
			}
		}
	}

	post {
		always {
			echo 'I run always'
		}
		success {
			echo 'I run when you are successful'
		}
		failure {
			echo 'I run when you fail'
		}
	}
}


