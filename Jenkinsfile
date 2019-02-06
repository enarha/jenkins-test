pipeline {
    agent any
    stages {
        stage('testing pipeline') {
            steps {
                echo "testing pipeline"
                sh "mkdir from-jenkins"
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
