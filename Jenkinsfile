pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git branch: 'main', url: 'https://github.com/tushardk058/devops_jenkins.git'
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
                bat 'npm test'
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