pipeline {
    agent any
    
    environment {
        DIRECTORY_PATH = '/path/to/source/code'
        TESTING_ENVIRONMENT = 'Staging'
        PRODUCTION_ENVIRONMENT = 'YourName'
    }
    
    stages {    // Multiple Stages
        stage('Build') {    //Single Stage
            steps {         //Add Steps to the stage    
                echo "Fetch the source code from the directory path: ${DIRECTORY_PATH}"
                echo "Compile the code and generate any necessary artifacts"
            }
        }
        
        stage('Test') {
            steps {
                echo "Unit tests"
                echo "Integration tests"
            }
        }
        
        stage('Code Quality Check') {
            steps {
                echo "Check the quality of the code"
            }
        }
        
        stage('Deploy') {
            steps {
                echo "Deploying to ${TESTING_ENVIRONMENT} environment"
            }
        }
        
        stage('Approval') {
            steps {
                echo "Waiting for manual approval to proceed to production deployment"
                sleep 10
            }
        }
        
        stage('Deploy to Production') {
            steps {
                echo "Deploying to production environment: ${PRODUCTION_ENVIRONMENT}"
            }
        }
    
        
    }
}
