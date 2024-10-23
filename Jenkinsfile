pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Check Status') {
            steps {
                bat 'git status'
            }
        }
        stage('Add Changes') {
            steps {
                bat 'git add .'
            }
        }
        stage('Commit Changes') {
            steps {
                script {
                    try {
                        bat 'git commit -m "Deployed using Jenkins"'
                    } catch (Exception e) {
                        echo "Error during git commit: ${e.message}"
                    }
                }
            }
        }
        stage('Push Changes') {
            steps {
                bat 'git push origin master'
            }
        }
    }
}
