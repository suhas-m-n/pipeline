pipeline {
    agent any

    environment {
        registry = 'majenayu/test_3'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/Majenayu/dock.git'
            }
        }

        stage('Build Image') {
            steps {
                script {
                    docker.build("${registry}")
                }
            }
        }
    }
}
