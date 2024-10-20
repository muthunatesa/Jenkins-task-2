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
                  subject: "Build successful",
		    body: "This build was successful"
	}
	failure {
		mail to: 'muthunatesa@gmail.com',
		   subject: "Build failed",
	 	     body: "This Build failed"
	}
   }
}

