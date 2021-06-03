pipeline {
  agent any
  triggers {
    githubPush()
  }
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
                sh 'cd UI; npm install -g mocha; npm install --production=false'
            }
             
        }
        stage('Test') {
            steps {
                echo 'Testing...'
				sh 'cd UI; npm test'
            }
            
        }
    }
}
