pipeline {
    
    agent any
    stages {
        stage("Clone docker-react from github") {
            steps {
                dir("docker-react") {
                    git(
                        url: "https://github.com/SoftBishop/docker-react.git",
                        branch: "master",
                        changelog: true,
                        poll: true
                    )
                }
            }
        }
        stage("Build docker") {
            steps{
                sh 'docker build -t softbishop/docker-react -f Dockerfile.dev .'
            }
        }
    }
}