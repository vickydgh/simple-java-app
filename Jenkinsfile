pipeline {
    agent any

    tools {
        // Define the Maven installation to use
        maven 'Maven 3.9.8'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Run Maven to compile the application
                bat 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Run Maven to execute tests
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deployment steps here
            }
        }
    }
}
