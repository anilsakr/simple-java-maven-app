pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'HELLO Build Notify'
        bitbucketStatusNotify ( buildState: 'INPROGRESS' )
        
        bitbucketStatusNotify ( buildState: 'SUCESS' )
      }
    

  }
}