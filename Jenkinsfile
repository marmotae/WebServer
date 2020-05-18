pipeline {
  agent any
  stages {
    stage('content') {
      parallel {
        stage('content') {
          steps {
            sh 'ls -la'
          }
        }

        stage('versions') {
          steps {
            sh 'git --version'
            sh 'docker --version'
          }
        }

      }
    }

    stage('message') {
      steps {
        echo 'Iniciando CI Process'
        sh 'docker build -t marmotae/webserver:v4 .'
      }
    }

  }
}