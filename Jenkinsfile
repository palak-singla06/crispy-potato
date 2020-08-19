pipeline {
    options {
        buildDiscarder(logRotator(numToKeepStr:'10'))
        timestamps()
    }
    agent any
    stages {
        stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
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
    post {
        success {
            echo 'Success'
        }
        failure {
            echo 'Failure'
        }
        unstable {
            echo 'Unstable'
        }
        always {
            echo 'Build Completed'
        }
    }
}