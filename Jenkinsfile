pipeline {
    agent any

    stages {


        stage('Test') {
            steps {
                 sh '''
                 python3 -m pip install --upgrade pip
                 pip3 install -r requirements.txt
                 python3 -m pytest -q test_app.py
                 '''
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
