// scripted pipeline

// Declarative pipeline

pipeline {
    agent { docker { image 'maven:3.8.6'} }
    stages {
        stage('Build') {
            steps {
                sh 'mvn --version'
                echo "Build"
                echo "BUILD_TAG - $env.BUILD_TAG"
            }
        }
        stage('Test') {
            steps {
                echo "Test"
            }
        }
        stage('Integration Test') {
            steps {
                echo "Integration Test"
            }
        }
       
    }
    post {
        always {
            echo "I run always"
        }
        success {
            echo "I run when you are successful"
        }
        failure {
            echo "I run when you fail"
        }
    }
}

