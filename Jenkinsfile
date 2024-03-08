pipeline {
    agent any 
    stages {
        /*
        stage('Clone repository') {
            steps {
                checkout([
                    $class: 'GitSCM', 
                    branches: [[name: '/main']], 
                    userRemoteConfigs: [[url: 'https://github.com/Jatinsharma159/Jenkins-git']]
                ])
            }
        }
        */
        stage('Build') {
            steps {
                build 'PES2UG21CS213-1'
                sh 'g++ main.cpp -o output'
                echo 'Build successful'
            }
        }    
        stage('Test') {
            steps {
                // Intentional error: incorrect command used
                sh './outpt'
                echo 'Test Stage Successful'
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
            error 'Pipeline failed'
        }
    }
}
