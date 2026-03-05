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
                sh 'test -f build/index.html'
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
