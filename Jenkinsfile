pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                
                bat 'echo "hello sahil we are Building the website..."'
            }
        }
        stage('Deploy') {
            steps {
                script {
                   
                    bat 'git config --global user.email "baadalrazz@gmail.com"'
                    bat 'git config --global user.name "sahilrazz"'
                    bat 'git add .'
                    // bat 'git commit -m "Deployed using jenkins "'
                    // bat 'git push origin master --force'
                }
            }
        }
    }
}
