pipeline {
    agent any

    stages {
        stage('kubectl get all') {
            steps {
               sh 'kubectl get all --namespace flask-space'
            }
        }
    }
}
