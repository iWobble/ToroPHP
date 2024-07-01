@Library('shared-pipeline') _

pipeline {
    agent any
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
