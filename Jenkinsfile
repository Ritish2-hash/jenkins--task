pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the application using Maven or Gradle...'
                }
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Executing unit and integration tests with JUnit or TestNG...'
                }
            }
        }
        
        stage('Code Quality Check') {
            steps {
                script {
                    echo 'Analyzing code quality using SonarQube...'
                }
            }
        }
        
        stage('Security Scan') {
            steps {
                script {
                    echo 'Conducting security scan with OWASP Dependency Check and Snyk...'
                }
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Deploying application to the staging environment using Docker and Kubernetes...'
                }
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Running automated tests on staging with Selenium and Postman...'
                }
            }
        }
        
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Rolling out deployment to production using Ansible and Kubernetes...'
                }
            }
        }
    }

    post {
        always {
            script {
                echo 'Sending pipeline completion notification via Jenkins email plugin...'
                mail (
                    subject: "Pipeline Notification: ${JOB_NAME} - Build #${BUILD_NUMBER}",
                    body: "The pipeline execution is complete. Check details here: ${BUILD_URL}",
                    to: 'ritish4803.be23@chitkara.edu.in'
                )
            }
        }
    }
}
