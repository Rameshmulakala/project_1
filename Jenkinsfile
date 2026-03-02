pipeline {
  agent { label 'Jenkins_agent }
  tools {
    jdk 'Java21'
    maven 'Maven3'
  }
  stages{
    stage("Cleanup Workspace"){
          steps {
            cleanWs()
          }
    }
    stage("checkout from SCM"){
        steps {
        git branch: 'main' , credentials: 'github' ,url: ''
        }
    }
  }
}
