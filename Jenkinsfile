
pipeline {
    agent {
        any {
            image 'docker:stable-dind'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    }
    stages {
        stage('Build and Push Docker Image') {
            steps {
                sh 'sudo apt-get install -y docker-compose'
                sh 'docker login -u furqanalihunzai -p Hunza123.'
                sh 'docker-compose build'
                sh 'docker-compose push'
            }
        }
    }
}
