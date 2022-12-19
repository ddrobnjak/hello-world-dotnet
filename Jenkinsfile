pipeline {
    agent any
    tools {
        dotnetsdk 'dotnet'
    }
    options {
        buildDiscarder(logRotator(numToKeepStr: '5'))
        disableConcurrentBuilds()
        skipDefaultCheckout()
    }
    stages {
        stage('Clean up') { 
            steps {
                deleteDir()
            }
        }
        stage('Clone') {
            steps {
                git credentialsId: '4f8dcf06-a320-4afd-914d-d7fa62be287c', url: 'git@github.com:ddrobnjak/hello-world-dotnet.git'
            }
        }
        stage('Build') {
            steps {
                sh 'dotnet build'
            }
        }      
    }
}
