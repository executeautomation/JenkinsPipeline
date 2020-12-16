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

        stage('Test log') {
          steps {
            writeFile(file: 'Testlog.txt', text: 'This is automation file')
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Do you want to deploy', id: 'Ok')
        echo 'Deploying Dot net Core'
      }
    }

  }
  environment {
    ChromeDriverPath = '/home/alex/.config/google-chrome'
  }
}