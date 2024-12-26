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
        stage('Docker Build') {
            steps {
                bat 'docker build -t my-node-app:latest .' 
            }
        }
        stage('Docker Run') { 
            steps {
                bat 'docker run -d -p 5000:5000 my-node-app:latest' 
            }
        }
    }
}

/* 

** Pipeline without Docker **

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

*/