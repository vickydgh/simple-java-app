pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/vickydgh/simple-java-app.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building...'
                // Replace with Windows-compatible build commands, if needed
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                // Replace with Windows-compatible test commands, if needed
                bat 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Replace with Windows-compatible deploy commands, if needed
                bat 'mvn deploy'
            }
        }
    }
}
