pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                cleanWs()
                echo 'Build stage'
            }
        }
        stage('Test') {
            steps {
                echo 'Test stage'
                sh 'npm test'
            }
        }
    }

    post {
        success {
            echo 'Success!'
        }
    }
}
