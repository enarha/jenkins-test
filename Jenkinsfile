/*
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
*/
node {
    stage('testing pipeline'){
        timestamps {
            if (env.BRANCH_NAME == 'master') {
                echo "working on branch master"
            } else {
                echo "working on branch different from master"
            }
            echo "testing pipeline"
            try {
                sh "mkdir -p from-jenkins"
                sh "touch from-jenkins/test.txt"
                sh "ls from-jenkins/non-existent.txt"
            } catch (Exception e) {
                println "Something went wrong! Recorded error: $e"
            }
        }
    }
    stage('saying goodbye') {
        timestamps {
            echo "goodbye from pipeline"
        }
    }
}
