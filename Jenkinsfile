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
                    echo 'Analyzing the code with SonarQube'
                    // sh 'sonar-scanner'
                }
            }
        }
        stage('Security Scan') {
            steps {
                script {
                    echo 'Performing Security Scan with OWASP Dependency-Check'
                    // sh 'dependency-check.sh'
                }
            }
        }
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Deploying to Staging server'
                    // sh 'aws deploy'
                }
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Running Integration Tests on Staging'
                    // sh 'selenium'
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Deploying to Production server'
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
