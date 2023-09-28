pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t mysql:latest ./db'
                'docker build -t flask-app:latest ./flask-app'
                'docker build -t nginx:latest ./nginx'
            }
        }
        
        stage('Push to Docker Hub') {
            steps {
                sh 'docker push esarkus/mysql:latest'
                sh 'docker push esarkus/flask-app:latest'
                sh 'docker push esarkus/nginx:latest'
            }
        }
    }
}
