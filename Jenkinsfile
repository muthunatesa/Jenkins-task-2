pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh './task_2.sh'
            }
        }
    }
    post {
        success {
            mail to: 'muthunatesa@gmail.com',
                 subject: 'Jenkins Build Success',
                 body: 'The build was successful.'
        }
        failure {
            mail to: 'muthunatesa@gmail.com',
                 subject: 'Jenkins Build Failure',
                 body: 'The build failed.'
        }
    }
}

