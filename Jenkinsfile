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
                // bat 'npm install'
                // bat 'npm run build'
                 // Modify the HTML file here
                // sh '''
                // # Define the file to modify
                // FILE="index.html"

                // // # Use sed to replace a placeholder or text in the HTML file
                // // # For example, replacing "PLACEHOLDER" with "Hello World!"
                // // sed -i 's/PLACEHOLDER/Hello World!/' $FILE

                // # Another example: inserting a timestamp in the HTML
                // echo "<!-- Build Time: $(date) -->" >> $FILE

                // # Validate the modification
                // cat $FILE
                // '''
            }
        }
        stage('Deploy') {
            steps {
                script {
                   
                    bat 'git config --global user.email "baadalrazz@gmail.com"'
                    bat 'git config --global user.name "sahilrazz"'
                    bat 'git add .'
                    bat 'echo "git commit -m "build done"'
                    bat 'echo "git push -U origin master"'
                    // bat 'git commit -m "Deployed using jenkins "'
                    // bat 'git push origin master --force'
                }
            }
        }
    }
}
