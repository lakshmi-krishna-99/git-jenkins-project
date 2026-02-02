pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'staging',
                    credentialsId: 'github-creds',
                    url: 'https://github.com/lakshmi-krishna-99/git-jenkins-project.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to staging environment...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}

