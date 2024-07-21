pipeline {
    agent any

    tools {
        // Specify the name of the Maven installation configured in Jenkins
        maven 'Maven 3.9.8'
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out the code...'
                // Checkout the code from your SCM
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Run Maven to compile the application
                bat 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Run Maven to execute tests
                bat 'mvn test'
            }
        }
        stage('Package') {
            steps {
                echo 'Packaging the application...'
                // Run Maven to package the application (e.g., create a JAR file)
                bat 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // Add your deployment steps here
                // Example: Copy the JAR file to a deployment directory or server
                // bat 'copy target\\myapp.jar C:\\deploy\\'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            // Clean up workspace or perform post-build actions
            cleanWs()
        }
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
