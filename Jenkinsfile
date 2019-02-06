/*
    pipeline starts here
*/
pipeline {
    agent any
    options {
        timestamps()
    }
    stages {
        // stage test
        stage('testing pipeline') {
            steps {
                echo "testing pipeline"
                sh "mkdir -p from-jenkins"
                sh "touch from-jenkins/test.txt"
            }
        }
        // stage end
        stage('saying goodbye') {
            steps {
                echo "goodbye from pipeline"
            }
        }
    }
}
