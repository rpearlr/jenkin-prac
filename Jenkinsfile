pipeline {
    agent any
     tools {
        jdk 'java21'         
        git 'Default'       
        python 'Python3'    
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
                    sh 'javac hello.java'
                    sh 'java Main'
                }
            }
        }

        stage('Python Program Execution') {
            steps {
                script {
                    echo 'Running Python Script...'
                    sh 'python3 hello1.py'
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
