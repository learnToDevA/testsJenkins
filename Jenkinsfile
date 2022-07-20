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
    stage('Ha after ending'){
      steps {
        echo "Ha - pipeline was edited using Jenkinse file in repo"
        echo "Real - infrastructure as a code :)"
        sh 'pwd'
        echo "Still in the same folder"
        echo "But with new env - check git diff :)"
        sh 'cat $newENV'
      }
    }

  }
  environment {
    fileToPrint = 'readme.md'
    newENV = 'someNewEnv'
  }
}