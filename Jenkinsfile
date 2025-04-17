pipeline {
    agent any

    tools {
        nodejs 'node18' 
    }
environment {
        GIT_CREDENTIALS_ID = "2dee6608-a49a-4ab0-90c0-3836e8f88c3b" // Use the ID from Step 1
        GIT_REPO = 'https://github.com/rajadevops2025/github.git'
        GIT_BRANCH = 'main'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: GIT_BRANCH, credentialsId: GIT_CREDENTIALS_ID, url: GIT_REPO
            }
        }
        stage('Build') {
            steps {
                bat 'npm install'
                bat 'node index.js'
            }
        }
    }
}
  
