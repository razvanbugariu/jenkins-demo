pipeline {
    agent any
    stages {
            stage('Build') {
                agent {
                    docker {
                        image 'maven:3.8.4-openjdk-11-slim'
                        // Run the container on the node specified at the
                        // top-level of the Pipeline, in the same workspace,
                        // rather than on a new node entirely:
                        reuseNode true
                    }
                }
                steps {
                    sh 'mvn -version'
                }
            }