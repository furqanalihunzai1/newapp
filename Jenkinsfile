
pipeline {
    agent {
        any {
            
            
        }
    }
    stages {
        stage('Build and Push Docker Image') {
            steps {
                
                sh 'docker login -u furqanalihunzai -p Hunza123.'
                sh 'docker compose build'
                sh 'docker compose push'
            }
        }
    }
}
