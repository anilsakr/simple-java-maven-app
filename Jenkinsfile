pipeline {
  agent any
  stages {
    stage('build') 
        bitbucketStatusNotify(
        buildState: 'INPROGRESS',
        buildKey: 'build',
        buildName: 'Build',
        repoSlug: 'simple-java-maven-app'   
      )
      try {
          myBuildFunction()
          bitbucketStatusNotify(
          buildState: 'SUCCESSFUL',
          buildKey: 'build',
          buildName: 'Build',
          repoSlug: 'simple-java-maven-app'          
          )
      } catch(Exception e) {
          bitbucketStatusNotify(
          buildState: 'FAILED',
          buildKey: 'build',
          buildName: 'Build',
          buildDescription: 'Something went wrong with build!',
          repoSlug: 'simple-java-maven-app' 
          )
      }
    

  }
}