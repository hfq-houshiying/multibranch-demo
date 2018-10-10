pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'pipeline {
    agent any
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh '/usr/local/bin/npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
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
npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
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
