pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project using Maven'
                    // sh 'mvn clean install'
                }
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Running Unit and Integration Tests with JUnit'
                    // sh 'mvn test'
                }
            }
        }
        stage('Code Analysis') {
            steps {
                script {
                    echo 'Running Code Analysis using SonarQube...'
                    // sh 'sonar-scanner'
                }
            }
        }
        stage('Security Scan') {
            steps {
                script {
                    echo 'Performing Security Scan using OWASP Dependency-Check...'
                    // sh 'dependency-check.sh'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Deploying the application to the Staging environment using AWS CLI...'
                    // sh 'aws deploy'
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Running Integration Tests on the Staging environment using Selenium...'
                    // sh 'selenium'
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Deploying the application to the Production environment using AWS CLI...'
                    // sh 'aws deploy'
                }
            }
        }
    }
    post {
        always {
            script {
                echo 'Sending email notification'
                //mail to: 'mabubakr9726@gmail.com', subject: "Build Status", body: "The build ${currentBuild.fullDisplayName} finished with status: ${currentBuild.currentResult}"
            }
        }
    }
}
