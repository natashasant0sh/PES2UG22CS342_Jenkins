pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ new.cpp -o PES2UG22CS342' 
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

        stge('Deploy') {
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
