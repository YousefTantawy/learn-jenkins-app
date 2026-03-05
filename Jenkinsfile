pipeline {
    agent any 
    stages {
        stage('Build') {
            steps {
                cleanWs()
                sh 'npm install'
                sh 'npm run build'
                echo 'Build stage'
            }
        }
        stage('Test') {
            agent {
                docker {
                    image 'node:18-alpine'
                }
            }
            steps {
                echo 'Test stage'
                sh 'npm test'
            }
        }
    }

    post {
        always {
            junit 'test-results/junit.xml'
        }
    }
}
