pipeline {
  agent any
  stages {
    stage('test001') {
      parallel {
        stage('test001') {
          steps {
            sh 'echo "test001"'
            build(job: 'test003', propagate: true)
          }
        }
        stage('test002') {
          environment {
            a = ''
            b = ''
          }
          steps {
            sleep 10
            sh 'echo "a: ${a}"'
          }
        }
      }
    }
    stage('test003') {
      environment {
        b = ''
      }
      steps {
        sh 'echo "b: ${b}"'
      }
    }
  }
}