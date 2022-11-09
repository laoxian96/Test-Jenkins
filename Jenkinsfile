#!/usr/bin/env groovy
pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh('npm install')
                sh('sudo pm2 start index.js')
                // sh("python3 /Users/moyi/.jenkins/workspace/Test/feishutongzhi.py $JOB_URL $JOB_NAME $BUILD_NUMBER")
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
