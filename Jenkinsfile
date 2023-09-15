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
                    docker.withRegistry('https://hub.docker.com', 'goran94hub') {
                        def customImage = docker.image('my-app-image:latest')
                        customImage.push()
                    }
                }
            }
        }
    }
}
