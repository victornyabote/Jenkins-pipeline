pipeline {
    agent any

    environment {
        DIRECTORY_PATH = '/my/project/code'
        TESTING_ENVIRONMENT = 'Testing'
        PRODUCTION_ENVIRONMENT = 'VictorProduction' //
    }

    stages {
        stage('Build') {
            steps {
                echo "Fetching source code from ${DIRECTORY_PATH}"
                echo "Compiling the code and generating artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "Running unit tests"
                echo "Running integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Checking quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying application to ${TESTING_ENVIRONMENT} environment"
            }
        }
        stage('Approval') {
            steps {
                echo "Waiting for manual approval"
                sleep 10
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying application to ${PRODUCTION_ENVIRONMENT} environment"
            }
        }
    }
}
