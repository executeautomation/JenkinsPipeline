pipeline {
   agent {
       label 'slave'
   }

   stages {
      stage('Hello') {
         steps {
                sh 'java -version'
                echo "Get working directory"
                sh 'pwd'
         }
      }
   }
}
