pipeline {
    
    agent any
    stages {
        stage("Build docker") {
            steps{
                //sh 'docker build -t softbishop/docker-react -f Dockerfile.dev .'
                docker.build("-t softbishop/docker-react -f Dockerfile.dev .")
            }
        }
    }
}