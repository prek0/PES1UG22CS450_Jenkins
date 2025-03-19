pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                    build 'PES1UG22CS450-1'
                    //sh 'g++ main_450.cpp -o output'
                    sh 'g++ main_45.cpp -o output'
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
