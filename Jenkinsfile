pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
                echo "hello world"
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                script {
                    sh "kubectl apply -f MyNginx/nginx.yaml"
                }
            }
        }
    }
}
