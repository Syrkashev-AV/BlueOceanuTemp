pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'This in build'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy to Dev1') {
          steps {
            sleep 30
            echo 'This to message'
          }
        }

        stage('Deploy to Dev_2') {
          steps {
            sleep 30
            echo 'compiled'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Testing'
      }
    }

  }
}