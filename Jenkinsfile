pipeline {
    agent any
    
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    bat 'docker build -t dhineshwaran/finalinternalassessment .'
                }
            }
        }
        
        stage('Publish Docker Image') {
            steps {
                script {
                    bat 'docker push dhineshwaran/finalinternalassessment:latest'
                }
            }
        }
        
        stage('Run Docker Container') {
            steps {
                script {
                    bat 'docker run --name finalserver -dit -p 5000:5000 dhineshwaran/finalinternalassessment'
                }
            }
        }
    }
}
