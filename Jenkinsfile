pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ new.cpp -o new'
                build 'PES1UG21CS618-1'
                echo 'Build stage successful'
            }
        }

        stage('Test') {
            steps {
                sh './test'
                echo 'Test stage successful'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
