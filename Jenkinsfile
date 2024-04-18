pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'helm version'
            }
        }
        stage('deploy') {
            sh 'helm install -f my-api/values.yaml my-api ./my-api'
        }
    }
}