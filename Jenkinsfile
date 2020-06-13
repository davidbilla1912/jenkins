pipeline {
     agent any
     stages {
	stage('Build') {
           steps {
		echo "Build"
	}
     }
     stage('test') {
           steps {
                echo "test"
        }
     }
     stage('integreation test') {
           steps {
                echo "integration test"
        }
     }


   }
   post {
     always {
        echo "alway"
     }
     success {
         echo "success"
     }
     failure {
         echo "failure"
     }
     changed {
         echo "changed"
     }
     unstable {
         echo "unstable"
     }
   }

}
