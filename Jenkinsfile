@Library('shared-pipeline') _

pipeline {
    agent any
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
        ansiColor('xterm')
    }
    stages {
        stage('Scan') {
            steps {
                sayHello()
                logInfo('logging INFO')
                logWarn('logging WARN')
                logError('logging ERROR')
                logDeprecated('logging Deprecated')
                withSonarQubeEnv(installationName: 'SonarQube', ) {
                    println "${env}"
                }
            }
        }
    }
}
