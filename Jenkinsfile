pipeline {
    agent { label 'docker' }
    stages {
        stage('Build') {
            steps {
                echo 'Build image'
                sh 'docker-compose build'
            }
        }
    }
    post {
        always {
            // Always cleanup after the build.
            sh 'docker-compose -f down'
            sh 'rm .env'
        }
    }
}
