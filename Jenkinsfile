pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/gs-sharma44648', branch: 'master', credentialsId: '2cfc8896-252a-4994-9061-85ad0cc719ac')
        sh 'echo "Hi, My name is Aishwarya"'
      }
    }

    stage('DeployDev') {
      parallel {
        stage('DeplyDev') {
          steps {
            sh 'echo: I will deploy the code in dev env"'
          }
        }

        stage('DeployQA') {
          steps {
            sh 'echo" I will deploy the code in QA env"'
          }
        }

      }
    }

  }
}