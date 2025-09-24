// This is a declarative pipeline that uses a Jenkins agent.
// The 'agent any' line tells Jenkins to run the pipeline on any available agent.
// For a real-world application, you might specify a Docker container image here.
// For example: agent { docker { image 'node:16-alpine' } }

pipeline {
    // Defines the agent where the pipeline will run.
    agent any

    // Defines the tools required for the pipeline.
    // These names must match the tool names configured in your Jenkins setup.
    tools {
        jdk 'Java 21'
        maven 'Maven 3'
    }

    // Defines the stages of the CI/CD pipeline.
    stages {
        // Stage 1: Checkout the code from the repository.
        stage('Checkout') {
            steps {
                echo 'Pulling the latest code from GitHub...'
                // Jenkins automatically checks out the code from the Git repository.
            }
        }

        // Stage 2: Build the application.
        // This stage compiles the code, resolves dependencies, and creates a build artifact.
        stage('Build') {
            steps {
                echo 'Building the application with Maven...'
                // The `bat` step is used to execute a Windows batch command.
                bat 'mvn clean package'
            }
        }

        // Stage 3: Test the application.
        // This stage runs automated unit tests.
        stage('Test') {
            steps {
                echo 'Running automated tests with Maven...'
                bat 'mvn test'
            }
        }

        // Stage 4: Deploy the application.
        // This stage deploys the built artifact.
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                // A simple placeholder for a real deployment action.
                bat 'echo "Deployment successful!"'
            }
        }
    }
}
