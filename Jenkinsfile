pipeline {
    agent any

    environment {
        DIRECTORY_PATH = "${WORKSPACE}"
        TESTING_ENVIRONMENT = "TestingEnvironment"
        PRODUCTION_ENVIRONMENT = "ASAD"
    }
    
    stages {
        stage('Build') {
            steps {
                echo "Building..."
            }
            post{
                always{
                    mail to: "asaddeakin.edu@gmail.com",
                    subject: "Build Status Email",
                    body: "Build log attached!"
                }
            }
        }
        stage('Build the code') {
            steps {
                echo "Building the code..."
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Running unit and integration tests ...."
            }
        }
        stage('Code Analysis') {
            steps {
                echo "Integrating a code analysis tool ..."
            }
        }
        stage('Security Scan') {
            steps {
                echo "Performing security scans using tools ..."
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo "Deploying the application ..."
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo "Running integration tests ...."
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying the application to a production server like AWS EC2 instance"
            }
        }
    }
}
