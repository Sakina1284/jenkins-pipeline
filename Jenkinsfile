pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building the code using Maven"
                    // Maven 
                }
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo "Running unit and integration tests"
                    // JUnit and Tricentis Tosca
                }
            }
            post {
                success {
                    mail to: 'sakeenanaleem123@gmail.com',
                         subject: "Status of Unit and Integration Tests: SUCCESS",
                         body: "The Unit and Integration Tests stage completed successfully."
                }
                failure {
                    mail to: 'sakeenanaleem123@gmail.com',
                         subject: "Status of Unit and Integration Tests: FAILURE",
                         body: "The Unit and Integration Tests stage failed. Please find the logs attached."
                }
            }
        }

        stage('Code Analysis') {
            steps {
                script {
                    echo "Performing code analysis"
                    // SonarQube and Codacy
                }
            }
        }

        stage('Security Scan') {
            steps {
                script {
                    echo "Performing security scan"
                    // OWASP ZAP
                }
            }
            post {
                success {
                    mail to: 'sakeenanaleem123@gmail.com',
                         subject: "Status of Security Scan: SUCCESS",
                         body: "The security scan stage completed successfully.\n\nCheck console output at $BUILD_URL to view the results."
                }
                failure {
                    mail to: 'sakeenanaleem123@gmail.com',
                         subject: "Status of Security Scan: FAILURE",
                         body: "The security scan stage failed. Please find the logs attached.\n\nCheck console output at $BUILD_URL to view the results."
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                script {
                    echo "Deploying the application to a staging server"
                    // Tool: Bamboo and AWS CodeDeploy
                }
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo "Running integration tests on staging"
                    // Katalon
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                script {
                    echo "Deploying the application to production"
                    // Ansible
                }
            }
        }
    }
}
