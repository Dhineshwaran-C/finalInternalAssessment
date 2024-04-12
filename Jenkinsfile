pipeline {
    agent any
    
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t dhineshwaran/finalInternalAssessment .'
                }
            }
        }
        
        stage('Publish Docker Image') {
            steps {
                script {
                    sh 'docker push dhineshwaran/finalInternalAssessment:latest'
                }
            }
        }
        
        stage('Run Docker Container') {
            steps {
                script {
                    sh 'docker run --name finalserver -dit -p 5000:5000 dhineshwaran/finalInternalAssessment'
                }
            }
        }
    }
}
