pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/saanyaaa/jenkins-demo.git'
            }
        }
        stage('Build') {
            steps {
                sh 'python3 -m py_compile app.py'
                echo 'Build successful'
            }
        }
        stage('Test') {
            steps {
                sh 'python3 app.py'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }
    post {
        success { echo 'Pipeline finished successfully' }
        failure { echo 'Pipeline failed' }
    }
}
