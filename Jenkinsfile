pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                echo 'Compiling the C++ program...'
                sh 'g++ -o hello_exec h.cpp'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running the program...'
                sh './hello_exec'
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
            echo 'Pipeline failed!'
        }
    }
}
