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
                sh 'cd test-nodeapp-1-task-2 && docker build . -t 130826749738.dkr.ecr.us-east-1.amazonaws.com/node:v${BUILD_NUMBER}'
                sh 'docker push 130826749738.dkr.ecr.us-east-1.amazonaws.com/node:v${BUILD_NUMBER}'
                sh 'docker rmi 130826749738.dkr.ecr.us-east-1.amazonaws.com/node:v${BUILD_NUMBER}'
            }
        }
        stage('docker deploy') { 
            steps {
                sh 'cd /home/ubuntu/ansible && ssh -i ubuntukey.pem ubuntu@10.0.1.198'
            }
        }
    }
}
