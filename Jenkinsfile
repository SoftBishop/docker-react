pipeline {
    agent any
    
    
    stages {
        stage("Build image from dockerfile") {
            steps{
                echo 'Start to build docker container!!!'
                //sh 'docker build -t softbishop/docker-react -f Dockerfile.dev .'
                script {
                    def dockerContainer = docker.build("-t softbishop/docker-react", "f Dockerfile.dev .")   
                }
            }
        }
    }
}