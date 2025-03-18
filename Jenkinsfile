pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                    build 'PES1UG22CS450-1'
                    sh 'g++ -o main_450.cpp -o output'
            }
        }
        
        stage('Test') {
            steps {
                    sh './output' 
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploy' 
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed :('
        }
    }
}
