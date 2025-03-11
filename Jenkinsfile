pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Compiling C++ file...'
                    sh 'g++ hello.cpp -o PES2UG22CS103-1'  // Compile the C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the compiled file...'
                    sh './PES2UG22CS103-1'  // Execute the compiled program
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    sh 'exit 1'  // **Intentional error: This forces the stage to fail**
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
            echo '❌ Pipeline failed at some stage!'
        }
    }
}
