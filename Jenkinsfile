pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Installing..'
        sh 'npm install'
      }
    }
    stage('Unit Tests') {
      steps {
        echo 'Executing Unit Tests..'
        sh 'npm test'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying....'
      }
    }
  }
  tools {
    nodejs 'default'
  }
}
