pipeline {
  agent any
  stages {
    stage('firststage') {
      parallel {
        stage('firststage') {
          steps {
            echo 'first-stage'
            bat 'ping -n 10 127.0.0.1'
            bat 'echo Success !'
          }
        }
        stage('first-parallel-stage') {
          steps {
            echo 'first-parallel-stage'
          }
        }
      }
    }
    stage('secondstage') {
      parallel {
        stage('secondstage') {
          steps {
            echo 'second-stage'
          }
        }
        stage('second-parallel-stage') {
          steps {
            echo 'second-parallel-stage'
          }
        }
      }
    }
    stage('third-stage') {
      steps {
        echo 'third-stage'
      }
    }
  }
}