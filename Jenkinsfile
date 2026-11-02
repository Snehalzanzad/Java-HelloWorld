
pipeline {
    agent any

    stages {

        stage('Git Checkout') {
            steps {
                echo 'Fetching code from GitHub'
                checkout scm
            }
        }

        stage('Compile Java') {
            steps {
                echo 'Compiling Java code'
                bat 'javac helloWorld.java'
            }
        }

        stage('Run Java') {
            steps {
                echo 'Executing Java program'
                bat 'java HelloWorld'
            }
        }
    }

    post {
        success {
            echo 'Java program executed successfully!'
        }

        failure {
            echo 'Java execution failed!'
        }
    }
}
