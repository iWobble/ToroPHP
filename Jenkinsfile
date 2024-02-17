pipeline {
  agent { label 'kube-agent' }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Scan') {
      steps {
        withSonarQubeEnv(installationName: 'SonarQube', ) {
          println ${env} 
        }
      }
    }
  }
}
