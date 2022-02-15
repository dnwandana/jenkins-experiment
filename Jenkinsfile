#!/usr/bin/env groovy

pipeline {
    agent {
        "node-1" {
            image 'golang:1.17.7-alpine'
            args '-u root'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'go build main.go'
            }
        }
        stage('Run') {
            steps {
                echo 'Testing the application...'
                sh 'go run main.go'
            }
        }
    }
}