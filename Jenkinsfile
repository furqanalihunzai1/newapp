pipeline {
    agent {
        any { }
    }
    stages {
        stage('Build and Push Docker Image') {
            steps {
                dir('./my-app') {
                    sh 'docker login -u furqanalihunzai -p Hunza123.'
                    sh 'docker build -f Dockerfile -t furqanalihunzai/frontend .'
                    sh 'docker push furqanalihunzai/frontend'
                }
                dir('./') {
                    sh 'docker build -f Dockerfile -t furqanalihunzai/backend .'
                    sh 'docker push furqanalihunzai/backend'
                }
                sh 'docker-compose -f docker-compose.yaml build'
                sh 'docker-compose -f docker-compose.yaml push'
            }
        }
       // stage('Run Tests') {
         //   steps {
           //     sh 'docker-compose -f docker-compose.yaml up -d'
             //   sh 'docker exec frontend npm run test'
               // sh 'docker exec backend python manage.py test'
              //  sh 'docker-compose -f docker-compose.yaml down'
           // }
       // }
    }
}
