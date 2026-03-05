pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Building application..."
                sh 'echo Build complete > output.txt'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'echo Tests passed'
            }
        }

        stage('Package') {
            steps {
                echo "Packaging application..."
                sh 'tar -czf app.tar.gz output.txt'
            }
        }

    }
}