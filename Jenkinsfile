pipeline {
    agent any 

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/maryembellil/nodesample.git' 
            }
        }
        stage('Build') {
            steps {
                bat 'npm install'
            }
        }
        stage('Test') {
            steps {
                bat 'npm test' 
            }
        }
        stage('Deploy') { 
            steps {
                bat 'npm start'
            }
        }
    }
}