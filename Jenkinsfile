pipeline {
    agent any

    tools {
        jdk 'Java 21'
        maven 'Maven 3'
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling the latest code from GitHub...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the application with Maven...'
                dir('my-cicd-app') {
                    bat 'mvn clean package'
                }
            }
        }

        stage('Test') {
            steps {
                echo 'Running automated tests with Maven...'
                dir('my-cicd-app') {
                    bat 'mvn test'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                bat 'echo "Deployment successful!"'
            }
        }
    }
}
