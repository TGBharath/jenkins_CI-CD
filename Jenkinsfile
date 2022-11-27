pipeline {
    agent any 
    stages {
        stage('git checkout') { 
            steps {
                checkout scm
            }
        }
        stage('docker build and push') { 
            steps {
                sh 'cd test-nodeapp-1-task-2 && ls'
            }
        }
    }
}
