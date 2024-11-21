pipeline {
    agent any

    stages {
        // Stage for GitHub Access (Job 1)
        stage('GitHub Access') {
            steps {
                script {
                    echo 'Accessing GitHub Repository...'
                    // Trigger Job 1: GitHub access (You can use a Jenkins job trigger here)
                    build job: 'Job1-GitHub-Access'
                }
            }
        }

        // Stage for Java Program Execution (Job 2)
        stage('Java Program Execution') {
            steps {
                script {
                    echo 'Running Java program...'
                    // Trigger Job 2: Java program execution
                    build job: 'Job2-Java-Execution'
                }
            }
        }

        // Stage for Python Program Execution (Job 3)
        stage('Python Program Execution') {
            steps {
                script {
                    echo 'Running Python program...'
                    // Trigger Job 3: Python program execution
                    build job: 'Job3-Python-Execution'
                }
            }
        }

        // Additional optional stages for Build, Test, or Deploy
        stage('Build') {
            steps {
                script {
                    // Build Docker image as per your original script
                    bat 'docker build -t my-nodejs-app .'
                }
            }
        }
        
        stage('Test') {
            steps {
                script {
                    // Run tests if you have any
                    echo 'Running tests...'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deploy the Docker image
                    echo 'Deploying application...'
                }
            }
        }
    }
}
