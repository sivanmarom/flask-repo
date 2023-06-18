pipeline {
    agent any

    stages {
        stage('build image') {
            steps {
               sh 'docker build -t flask-frontend:${params.flask_version} .'
            }
        }
        stage('flask deploy') {
            steps {
               sh 'kubectl apply -f flask-deployment.yaml'
            }
        }
        stage('kubectl get all') {
            steps {
               sh 'kubectl get all --namespace flask-space'
            }
        }
    }
}
