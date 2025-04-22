/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'maven:3.9.9-eclipse-temurin-21-alpine' } }
    stages {
        stage('Checkout') {
            steps {
                git(
                    url: 'https://github.com/your-org/your-repo.git',
                    credentialsId: 'github-pat',  // 替换为你的凭证ID
                    branch: 'main'
                )
            }
        }
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}