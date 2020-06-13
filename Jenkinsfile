pipeline {
     agent { docker { image 'maven:3.6.3'}  }
     stages {
	stage('Build') {
           steps {
                sh 'mvn --version'
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
