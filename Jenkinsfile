pipeline {
    
    agent any
    
    stages {
        stage('pre-build cleanup') {
            steps {
                sh 'docker system prune -f'
            }
        }    
        
        stage('build and run containers') {
            steps {
                sh '''
                docker build -t gcr.io/lbg-mea-11/sprint3_sweta:v2 .
                docker push gcr.io/lbg-mea-11/sprint3_sweta:v2 .
                '''
            }
        }
    }
}   
