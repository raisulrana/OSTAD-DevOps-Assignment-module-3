pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/raisulrana/OSTAD-Assignment-module-3.git'
            }
        }

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm run check'
            }
        }
    }

    post {
        success {
            echo 'Build succeeded.'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
