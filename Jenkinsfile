pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build completed'
      }
    }

    stage('Test Stages') {
      parallel {
        stage('Test 2') {
          steps {
            echo 'running test2'
          }
        }

        stage('Test 1') {
          steps {
            echo 'running test1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'deployment complited'
      }
    }

  }
}