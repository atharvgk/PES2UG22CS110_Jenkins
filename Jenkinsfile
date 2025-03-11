// pipeline {
//     agent any

//     stages {
//         stage('Build') {
//             steps {
//                 script {
//                     echo 'Compiling C++ file...'
//                     sh 'g++ ./main/hello.cpp -o PES2UG22CS110-1'
//                 }
//             }
//         }

//         stage('Test') {
//             steps {
//                 script {
//                     echo 'Running the compiled file...'
//                     sh './PES2UG22CS110-1'
//                 }
//             }
//         }

//         stage('Deploy') {
//             steps {
//                 script {
//                     echo 'Deploying the application...'
//                 }
//             }
//         }
//     }

//     post {
//         always {
//             echo 'Pipeline execution completed.'
//         }
//         success {
//             echo 'Pipeline executed successfully!'
//         }
//         failure {
//             echo 'Pipeline failed at some stage!'
//         }
//     }
// }


pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Compiling C++ file...'
                    sh 'g++ ./main/hello.cpp -o PES2UG22CS110-1'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the compiled file...'
                    sh './PES2UG22CS110-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    sh 'exit 1'
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