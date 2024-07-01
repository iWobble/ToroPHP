@Library('shared-pipeline') _

pipeline {
  //dagent { label 'kube-agent' }
  options {
    buildDiscarder(logRotator(numToKeepStr: '5'))
  }
  stages {
    stage('Scan') {
      steps {
        sayHello()
        withSonarQubeEnv(installationName: 'SonarQube', ) {
          println "${env}"
        }
      }
    }
  }
}
