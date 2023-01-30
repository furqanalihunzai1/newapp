pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker rmi furqanalihunzai/assignment:latest -f'
                sh 'docker build -t furqanalihunzai/assignment:latest . '
            }
        }
        
        stage('login') {
            steps {
                sh 'docker login -u furqanalihunzai -p Furqan1111'
           }
        }
        
        stage('push') {
            steps {
        sh 'docker push furqanalihunzai/assignment:latest'
      
            }
        }   
        
       }    
}
