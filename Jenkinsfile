pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Compiling C++ file...'
                    sh 'gcc hello.cpp -o PES2UG22CS110-1'  // Compile the C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the compiled file...'
                    sh './PES2UG22CS110-1'  // Execute the compiled program
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                }
            }
        }
    }

    post {
        always {
            echo 'Pipeline execution completed.'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed at some stage!'
        }
    }
}