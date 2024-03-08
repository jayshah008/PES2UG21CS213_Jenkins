pipeline {
  agent any 
  stages {
//        stage('Clone repository') {
//        steps {
//          checkout ([Sclass: 'GitSCM', 
//          branches: [[name: '*/main']l, 
//          userRemoteConfigs: [[url: *https: //github.com/Jatinsharma159/Jenkins-git']ll)
//        }
//      }
    stage ('Build') {
      steps {
        build 'PES2UG21CS213-1'
        sh 'g++ main.cpp -o output'
        echo 'build successful'
      }
    }    
    stage( 'Test') {
      steps {
        sh './output'
        echo 'Test Stage Successful'
      }
    }
    stage ('Deploy') (
      steps {
        echo 'deploy'
      }
    }
    post{
      failure{
        error 'Pipeline failed'
      }
    }
}
