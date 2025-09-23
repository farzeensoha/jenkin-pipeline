// This is a declarative pipeline that uses a Jenkins agent.
// The 'agent any' line tells Jenkins to run the pipeline on any available agent.
// For a real-world application, you might specify a Docker container image here.
// For example: agent { docker { image 'node:16-alpine' } }

pipeline {
// Defines the agent where the pipeline will run.
agent any

// Defines the stages of the CI/CD pipeline.
stages {
    // Stage 1: Build the application.
    // This stage would typically compile code, resolve dependencies, and create an artifact.
    stage('Build') {
        steps {
            // Use the `sh` step to execute a shell command.
            // Replace this with your actual build command (e.g., `npm install`, `mvn package`, `docker build . -t my-app`).
            echo 'Building the application...'
            sh 'echo "Build successful!"'
            // Example of a Docker build:
            // sh 'docker build -t my-app:latest .'
        }
    }

    // Stage 2: Test the application.
    // This stage runs automated unit tests, integration tests, or security scans.
    stage('Test') {
        steps {
            echo 'Running automated tests...'
            // Replace this with your actual test command (e.g., `npm test`, `pytest`).
            sh 'echo "Tests passed!"'
        }
    }

    // Stage 3: Deploy the application.
    // This stage deploys the built artifact to a target environment (e.g., dev, staging, production).
    stage('Deploy') {
        steps {
            echo 'Deploying to the production environment...'
            // Replace this with your actual deployment command (e.g., `ssh user@server "cd /path && ./start-app.sh"`,
            // `docker push my-app:latest`, or using a deployment plugin).
            sh 'echo "Deployment successful!"'
        }
    }
}

}