pipeline {
    agent any
    options {
        timestamps()
    }
    stages {
        stage('testing pipeline') {
            steps {
                echo "testing pipeline"
                sh "mkdir -p from-jenkins"
                sh "touch from-jenkins/test.txt"
            }
        }
        stage('saying goodbye') {
            steps {
                echo "goodbye from pipeline"
            }
        }
    }
}
