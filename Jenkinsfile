pipeline {

  agent any

  options {

    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')

  }

  stages {

    stage('Hello') {

      steps {

        echo 'Deploying only From Feature Branch...'

      }

    }
    
     stage('Deploy') {
            when { tag "release-*" }
            steps {
                echo 'Able to find the release tag so running this stage'
                
            }
        }

  }

}
