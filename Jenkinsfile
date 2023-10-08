pipeline {
    agent any
    options {
        ansiColor('xterm')
    }
    stages {
        stage("Build image from dockerfile") {
            steps{
                echo 'Start to build docker container!!!'
                sh 'docker build -t softbishop/docker-react -f Dockerfile.dev .'
            }
        }
        stage("Test stage") {
            steps{
                sh 'docker run softbishop/docker-react npm run test -- --watchAll=false --coverage'
            } 
        }
    }
}