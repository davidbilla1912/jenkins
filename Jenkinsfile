pipeline {
     agent any
    // environment {
      //  dockerHome = tool "mydocker"
       //  mavenHome = tool "mymaven"
        // PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
    // }
     stages {
	stage('Build') {
           steps {
                echo "BUILD TAG - $env.BUILD_TAG"
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

        stage ('Build docker imge') {
           steps {
             script {
               dockerimage = docker.build("sundarhub/currency-exchange:${env.BUILD_TAG}")
            }
        }

   }
        stage ('push docker image') {
           steps {
              script {
                 docker.withRegistry('', 'dockerhub') {
                 dockerImage.push();
                 dockerImage.push('latest');
           }
         }
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
