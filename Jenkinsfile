pipeline {
  agent any
  stages {
    stage('Printing file ') {
      steps {
        echo 'Begin of pipeline'
        sh '''cat \'readme.md\'

'''
        sh 'pwd'
      }
    }

    stage('Some env tests') {
      steps {
        sh 'pwd'
        sh 'cat $fileToPrint'
        sh 'echo $fileToPrint'
      }
    }

    stage('Ending') {
      steps {
        echo 'End of pipeline'
      }
    }

  }
  environment {
    fileToPrint = 'readme.md'
  }
}