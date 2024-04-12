pipeline {
    agent any
    
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    bat 'docker build -t dhineshwaran/finalInternalAssessment .'
                }
            }
        }
        
        stage('Publish Docker Image') {
            steps {
                script {
                    bat 'docker push dhineshwaran/finalInternalAssessment:latest'
                }
            }
        }
        
        stage('Run Docker Container') {
            steps {
                script {
                    bat 'docker run --name finalserver -dit -p 5000:5000 dhineshwaran/finalInternalAssessment'
                }
            }
        }
    }
}
