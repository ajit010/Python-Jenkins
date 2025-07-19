pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/yourusername/git-jenkins-demo.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build("git-jenkins-demo:${env.BUILD_ID}")
                }
            }
        }
        stage('Run Tests') {
            steps {
                sh 'echo "No tests yet, but you can add!"'
            }
        }
    }
}
