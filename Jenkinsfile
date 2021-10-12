pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                bat 'npm install'
                bat 'yarn build'
            }
        }
        stage('Test') {
            steps {
                bat 'yarn test'
            }
        }
        stage('Deploy'){
            steps {
                bat 'serve -s build'
            }
        }
    }
}   