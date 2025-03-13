pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ wrong.cpp -o PES2UG22CS342' // Intentional error: wrong file name
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES2UG22CS342' 
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
            echo 'Pipeline failed'
        }
    }
}
