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
                sh 'npm install' 
            }
        }
        stage('Test') {
            steps {
                sh 'npm test' 
            }
        }
        stage('Deploy') { 
            steps {
                // Your deployment steps here (e.g., copy files to server)
            }
        }
    }
}