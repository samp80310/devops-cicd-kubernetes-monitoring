pipeline {
    agent any

    stages {

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t samp80310/devops-demo-app:latest .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push samp80310/devops-demo-app:latest'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f kubernetes/'
            }
        }

    }
}
