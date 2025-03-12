pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using a shell script
                    sh 'g++ -o hello hello.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Print output of the .cpp file
                    sh './hello'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // You can add your deploy steps here if required
                    echo 'Deploying... (this can be an empty step for now)'
                }
            }
        }
    }

    post {
        failure {
            // Print message if the pipeline fails
            echo 'Pipeline failed'
        }
    }
}
