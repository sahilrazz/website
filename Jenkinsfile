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
                
                sh 'echo "hello sahil we are Building the website..."'
            }
        }
        stage('Deploy') {
            steps {
                script {
                   
                    sh 'git config --global user.email "baadalrazz@gmail.com"'
                    sh 'git config --global user.name "sahilrazz"'
                    sh 'git add .'
                    sh 'git commit -m "Deployed using jenkins "'
                    sh 'git push origin master --force'
                }
            }
        }
    }
}
