pipeline {
  agent { label 'Jenkins_agent' }
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
        git branch: 'main' , credentials: 'github' ,url: 'https://github.com/Rameshmulakala/project_1.git'
        }
    }
    stage ("Built Application"){
      steps{
        sh "mvn clean package"
      }
    }
    stage ("Test Application"){
      steps{
        sh "mvn test"
      }
    }
  }
}
