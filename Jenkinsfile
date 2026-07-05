pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Bhoom-jpg/TechNova.git'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t technova-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh '''
                docker stop technova-app || true
                docker rm technova-app || true
                docker run -d -p 5000:5000 --name technova-app technova-app
                '''
            }
        }
    }
}
