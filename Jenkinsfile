pipeline {
    agent any
    environment {
        CI = 'true'
        PATH = "$PATH:/usr/local/bin"
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'test'
            }
        }
        stage('Deliver for development') {
            when {
                branch 'development' 
            }
            steps {
                echo 'deploy development'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh 'echo "kill old progress"'
            }
        }
        stage('Deploy for staging') {
            when {
                branch "feature/*" 
            }
            steps {
                echo 'deploy development'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh 'echo "kill old progress"'
            }
        }
        stage('Deploy for production') {
            when {
                branch 'master'  
            }
            steps {
                echo 'deploy production'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh 'echo "kill old progress"'
            }
        }
    }
}
