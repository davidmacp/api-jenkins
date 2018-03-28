pipeline {
  agent any
  stages {
    stage('Unit Tests') {
      steps {
        sh '''export PATH=$PATH:/Users/Shared/Jenkins/Home/tools/jenkins.plugins.nodejs.tools.NodeJSInstallation//default/bin
echo $PATH
node -v
npm -v
npm install
npm test'''
      }
    }
  }
}