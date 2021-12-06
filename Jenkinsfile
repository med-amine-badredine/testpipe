pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build completed'
        retry(count: 3) {
          sh 'wwwwww'
        }

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
        input(message: 'are you sure to deploy ', ok: 'yes i\'m sure')
      }
    }

    stage('notify for new build') {
      steps {
        echo 'new build completed.'
      }
    }

  }
}