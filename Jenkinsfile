pipeline {
  agent any
  stages {
    stage('build') {
      bitbucketStatusNotify(
      buildState: 'SUCCESSFUL',
      repoSlug: 'simple-java-maven-app',
      echo 'to get commit ID'
      shortCommit = sh(returnStdout: true, script: "git log -n 1 --pretty=format:'%h'").trim()
      commitId: ${shortCommit}      
      )
      steps {
        echo 'Hello From Build Notify..'
      }
    }
  }
}