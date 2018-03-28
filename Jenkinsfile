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
    stage('Browser Tests') {
      parallel {
        stage('Chrome') {
          steps {
            echo 'Executing Chrome Tests...'
          }
        }
        stage('Firefox') {
          steps {
            echo 'Executing Firefox Tests...'
          }
        }
        stage('Safari') {
          steps {
            echo 'Executing Safari Tests..'
          }
        }
      }
    }
    stage('BETA/QA') {
      steps {
        echo 'Executing BETA/QA Tests...'
      }
    }
    stage('Go/No Go') {
      steps {
        input(message: 'Ready to launch?', ok: 'Drop the bomb!')
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploying...'
      }
    }
  }
  tools {
    nodejs 'default'
  }
}