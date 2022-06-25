pipeline {
  agent any
  stages {
    stage('Git checkout') {
      steps {
        echo 'Checkout'
        sleep 1
      }
    }

    stage('Initiate') {
      steps {
        echo 'Initialize'
      }
    }

    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Building'
            sleep 2
            echo 'Build success'
          }
        }

        stage('Test') {
          steps {
            echo 'Unit tests'
          }
        }

        stage('Sonar') {
          steps {
            echo 'Sonar analysis'
          }
        }

      }
    }

    stage('Package') {
      steps {
        echo 'Packaging'
      }
    }

    stage('Baseline update') {
      steps {
        echo 'Bom updated'
      }
    }

    stage('Deploy') {
      steps {
        echo 'War deployed'
      }
    }

  }
}