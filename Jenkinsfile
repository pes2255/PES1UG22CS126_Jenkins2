pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output hello.cpp'  // Compiling the .cpp file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'  // Running the compiled output file
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Successful!'  // Simple success message
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'  // Post-action for failure handling
        }
    }
}
