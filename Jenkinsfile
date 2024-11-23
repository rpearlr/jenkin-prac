pipeline {
    agent any
    stages {
        stage('Git Checkout') {
            steps {
                echo 'Cloning Repository...'
                git branch: 'main', url: 'https://github.com/<your-username>/<your-repo>.git'
            }
        }

        stage('Java Program Execution') {
            steps {
                script {
                    echo 'Running Java Program...'
                    sh 'javac Main.java'
                    sh 'java Main'
                }
            }
        }

        stage('Python Program Execution') {
            steps {
                script {
                    echo 'Running Python Script...'
                    sh 'python3 script.py'
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