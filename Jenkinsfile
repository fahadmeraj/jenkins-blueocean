pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat 'dir'
      }
    }

    stage('print command') {
      parallel {
        stage('print command') {
          steps {
            echo 'test'
          }
        }

        stage('error') {
          steps {
            echo 'test parralel'
          }
        }

      }
    }

    stage('deploy') {
      agent any
      steps {
        echo 'deploying'
      }
    }

    stage('prod') {
      steps {
        echo 'prod'
      }
    }

  }
}