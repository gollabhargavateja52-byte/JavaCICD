
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/gollabhargavateja52-byte/JavaCICD.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
    }

    post {
        success {
            echo 'Java CI/CD Pipeline completed successfully!'
        }

        failure {
            echo 'Java CI/CD Pipeline failed. Check the console output.'
        }
    }
}
