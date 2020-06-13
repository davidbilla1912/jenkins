pipeline {
     agent any
     environment {
        dockerHome = tool "mydocker"
        mavenHome = tool "mymaven"
        PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
    }
     stages {
	stage('Build') {
           steps {
                sh 'mvn --version'
                docker 'docker version'
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
