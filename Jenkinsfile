pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ PES1UG20CS470.cpp -o PES1UG20CS470_t5'
                build job: 'PES1UG20CS470-1'
            }
        }
        
        stage('Test') {
            steps {
                sh './PES1UG20CS470_5'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deployment successful'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
