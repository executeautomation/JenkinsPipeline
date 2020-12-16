pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building a Dot Ner Core'
          }
        }

        stage('Test') {
          steps {
            echo "Get Driver Path ${ChromeDriverPath}"
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploying Dot net Core'
      }
    }

  }
  environment {
    ChromeDriverPath = '/home/alex/.config/google-chrome'
  }
}