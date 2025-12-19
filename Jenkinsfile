pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t devops-demo:latest .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run --rm devops-demo:latest'
            }
        }
    }
}
