pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/tushardk058/devops_jenkins'
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run Application') {
            steps {
                bat 'node app.js'
            }
        }
         stage('Run Tests') {
            steps {
                bat 'node test'
            }
        }
    }
    post {
        success{
            echo 'CI Pipeline Success'
        }
         failure{
            echo 'CI Pipeline Fail'
        }
    }
}