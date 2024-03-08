pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''pwd
date
'''
      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'test start'
          }
        }

        stage('parallel - test') {
          steps {
            echo 'test parallel execution'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sh 'pwd'
        echo 'deploy ready'
        sleep 30
      }
    }

  }
}