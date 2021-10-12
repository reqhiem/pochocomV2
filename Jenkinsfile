pipeline {
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install',
                sh 'yarn build'
            }
        }
        stage('Test') {
            steps {
                sh 'yarn test'
            }
        }
        stage('Deploy'){
            steps {
                sh 'serve -s build'
            }
        }
    }
}   