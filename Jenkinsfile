pipeline {
  agent any
  stages {
    stage(' Build') {
      steps {
        echo 'Build done successfully'
      }
    }

    stage('DEV') {
      parallel {
        stage('DEV') {
          steps {
            echo 'DEV deploy'
          }
        }

        stage('QA') {
          steps {
            echo 'QA done'
          }
        }

      }
    }

    stage('Prod') {
      steps {
        echo 'Prod done'
      }
    }

  }
}