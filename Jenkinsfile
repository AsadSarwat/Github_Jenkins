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
        stage('Build') {
            steps {
                echo "Building the code using Maven or any other build automation tool"
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo "Running unit and integration tests using test automation tools like JUnit or TestNG"
            }
        }
        stage('Code Analysis') {
            steps {
                echo "Integrating a code analysis tool like SonarQube or Checkstyle to analyze the code"
            }
        }
        stage('Security Scan') {
            steps {
                echo "Performing security scans using tools like OWASP ZAP or SonarQube Security Plugin"
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo "Deploying the application to a staging server like AWS EC2 instance"
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo "Running integration tests on the staging environment"
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying the application to a production server like AWS EC2 instance"
            }
        }
    }
}
