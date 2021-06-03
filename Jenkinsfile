pipeline {
  agent any
    tools {nodejs "NodeJs"}
    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout...'
                sh 'rm -rf UI; git clone https://github.com/jeisonroa1/movie-analyst-ui.git UI'
            }
            
        }
        stage('Build') { 
            steps {
                echo 'Build...'
                sh 'cd UI; npm install'
            }
             
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh 'npm test'
            }
            
        }
    }
}