node {
    stage {
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

node {
   stage('Preparation') { // for display purposes
      // Get some code from a GitHub repository

       git(
       url: 'git 'git@bitbucket.org:dvcsolutions/test-app.git'',
       credentialsId: 'MilanDVC',
       branch: "master"
    )'
   }
   stage('Build') {
      echo 'Build image'
      sh 'docker-compose build'
   }
   stage('Results') {

   }
   stage('Deploy') {
       
   }
}
