pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'build command'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'run par1'
          }
        }

        stage('testpar') {
          steps {
            echo 'run par2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'deploy'
        sleep 10
      }
    }

  }
}