pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t my-app-image:latest .'
            }
        }

        stage('Push Docker Image to Registry') {
            steps {
                script {
		    sh 'docker login -u goran94hub -p sisajkaru93'
		    sh 'docker push goran94hub/my-app-image:latest'                    
                    }
                }
            }
        }
    }
}
