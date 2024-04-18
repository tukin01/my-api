pipeline {
    agent any
    environment {
        KUBECONFIG = credentials('kubernetes-config')
    }
    stages {
        stage('build') {
            steps {
                sh 'helm version'
            }
        }
        stage('deploy') {
            steps {
                sh 'helm install -f my-api/values.yaml my-api ./my-api'
            }

        }
    }
}