pipeline {
    agent any

    environment {
        // You can define some environment variables if needed
        PROJECT_NAME = "Webhook-Test-Project"
    }

    stages {
        stage('Start') {
            steps {
                echo "🔧 Starting the Webhook Test Pipeline for ${env.PROJECT_NAME}"
            }
        }

        stage('Checkout') {
            steps {
                echo "📦 Checking out source code..."
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "🔨 Simulating build process..."
                // Simulate a build with a sleep
                sh 'sleep 2'
            }
        }

        stage('Test') {
            steps {
                echo "✅ Running tests..."
                // Simulate tests with a sleep
                sh 'sleep 2'
            }
        }

        stage('Info') {
            steps {
                echo "🧾 Environment Info:"
                echo "Branch: ${env.GIT_BRANCH}"
                echo "Commit: ${env.GIT_COMMIT}"
                echo "Build number: ${env.BUILD_NUMBER}"
            }
        }
    }

    post {
        always {
            echo "🏁 Webhook test pipeline completed for ${env.PROJECT_NAME}"
        }
    }
}

