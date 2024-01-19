pipeline {
  agent any
  stages {
    stage('Dev') {
      parallel {
        stage('Dev') {
          steps {
            git(url: 'https://github.com/anilkpo/MypythonCode.git', branch: 'master', changelog: true, poll: true)
          }
        }

        stage('Test') {
          steps {
            sh 'echo "This is test"'
          }
        }

      }
    }

    stage('Final') {
      steps {
        echo 'This is final'
      }
    }

  }
}