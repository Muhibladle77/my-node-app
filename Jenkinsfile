pipeline {
    agent any

    stages {
        // Stage for GitHub Access (Job 1)
        stage('GitHub Access') {
            steps {
                script {
                    echo 'Accessing GitHub Repository...'
                    // Clone the GitHub repository
                    git 'https://github.com/Muhibladle77/my-node-app.git'
                }
            }
        }

        // Stage for Java Program Execution (Job 2)
        stage('Java Program Execution') {
            steps {
                script {
                    echo 'Running Java program...'

                    // Ensure Java is installed
                    bat 'java -version'

                    // Compile the Java program (adjust the file name accordingly)
                    bat 'javac YourJavaProgram.java'

                    // Run the Java program
                    bat 'java YourJavaProgram'
                }
            }
        }


        // Additional optional stages for Build, Test, or Deploy
        stage('Build Docker Image') {
            steps {
                script {
                    // Build Docker image as per your original script
                    bat 'docker build -t my-nodejs-app1 .'
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
