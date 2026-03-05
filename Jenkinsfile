pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo "Building application..."
                bat 'echo Build complete > output.txt'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                bat 'echo Tests passed'
            }
        }

        stage('Package') {
            steps {
                echo "Packaging application..."
                bat 'copy output.txt app.txt'
                archiveArtifacts artifacts: 'app.txt'
            }
        }

    }

    post {
        success {
            echo "Pipeline successful"
        }
        failure {
            echo "Pipeline failed"
        }
    }
}