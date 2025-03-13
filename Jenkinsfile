pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output YOUR_SRN-1.cpp'  // Compile C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'  // Run the compiled program
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
