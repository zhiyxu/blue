pipeline {
  agent any
  stages {
    stage('test001') {
      parallel {
        stage('test001') {
          steps {
            sh 'echo "test001"'
          }
        }
        stage('test002') {
          steps {
            sleep 10
          }
        }
      }
    }
  }
}