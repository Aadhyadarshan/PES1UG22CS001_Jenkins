
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ hello.cpp -o hello_exec'  // Removed "main/"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './hello_exec'  // Removed "main/"
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
