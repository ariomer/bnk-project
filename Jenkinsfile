pipeline {
    agent { label "master" }
    
    stages {
        stage('Build Docker Image') {
            steps {
                sh 'docker-compose up'
                sh 'docker image ls'
            }
        }

    }
    post {
        always {
            echo 'Deleting all local images'
            sh 'docker image prune -af'
        }
        changed {
            echo 'down all local images'
            sh 'docker-compose down'
        }
    }
}