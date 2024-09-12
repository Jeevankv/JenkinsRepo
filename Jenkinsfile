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
        mail(subject: 'Build done ', body: 'Jenkins', from: 'jeevankv18@gmail.com', to: 'jeevankv2000@gmail.com')
      }
    }

  }
}