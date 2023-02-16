pipeline {
  agent any
    stages {
      stage('Build') {
        steps {
          sh 'g++ main/hello.cpp'
          build 'PES1UG21CS812-1'
        }
      }
      stage('Test') {
        steps {
          sh './a.out'
        }
      }
      stage('Deploy') {
        steps {
          echo 'Application is deployed'
        }
      }
    }
    post {
      failure{
        echo 'Pipeline failed'
      }
    }
  }
