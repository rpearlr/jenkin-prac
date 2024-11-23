pipeline {
    agent any
     tools {
        jdk 'java21'         
    }
    stages {
        stage('Git Checkout') {
            steps {
                echo 'Cloning Repository...'
                git branch: 'main', url: 'https://github.com/rpearlr/jenkin-prac.git'
            }
        }

        stage('Java Program Execution') {
            steps {
                script {
                    echo 'Running Java Program...'
                    bat 'javac hello.java'
                    bat 'java hello'
                }
            }
        }

        stage('Python Program Execution') {
            steps {
                script {
                    echo 'Running Python Script...'
                    bat 'python3 hello1.py'
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline Execution Complete.'
        }
    }
}
