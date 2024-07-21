pipeline {
agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Compile the Java application
                sh 'ant compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Here you would add steps to run your tests
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Here you would add steps to deploy your application
            }
        }
    } 
} 
