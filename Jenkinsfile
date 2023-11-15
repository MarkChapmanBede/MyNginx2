pipeline {
    agent any
    
    stages {
        stage('Checkoutt') {
            steps {
                checkout scm
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                script {
                    // Apply the Kubernetes manifests
                    sh "kubectl apply -f /var/lib/jenkins/workspace/MCKubes/nginx.yaml"
                    sh "kubectl apply -f /var/lib/jenkins/workspace/MCKubes/ServiceLB.yaml"
                }
            }
        }
    }
}
