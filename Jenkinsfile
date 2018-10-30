pipeline {
  agent any
  stages {
    stage('SCA') {
      parallel {
        stage('SCA') {
          steps {
            sh 'echo "Test"'
          }
        }
        stage('build') {
          steps {
            echo 'Building'
          }
        }
      }
    }
    stage('FT') {
      parallel {
        stage('FT') {
          steps {
            echo 'Functional test'
          }
        }
        stage('Perf') {
          steps {
            echo 'Perf'
          }
        }
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy'
      }
    }
  }
}