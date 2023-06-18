pipeline {
    agent any

    stages {
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
