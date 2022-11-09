#!/usr/bin/env groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh('pm2 delete all')
                sh('npm install')
                sh('pm2 start index.js')
                sh("python3 /Users/moyi/.jenkins/workspace/Test/feishutongzhi.py $JOB_URL $JOB_NAME $BUILD_NUMBER")
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
