pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Build your Docker image
                sh 'docker build -t my-app-image .'
            }
        }

        stage('Test') {
            steps {
                // Run your application tests
                sh 'docker run my-app-image tests'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy your application to a non-production environment
                sh 'docker-compose up -d'
            }
        }
    }
}
