
pipeline {
  agent { label 'Jenkins-Agent' }
  tools {
    jdk 'Java17'
    maven 'Maven3'   
  }
  stages{
    stage("Cleanup the Workspace"){
          steps{
            cleanWs()
          }
    }
    stage("Git checkout"){
          steps{
            git branch: 'main', credentialsId: 'github', url: 'https://github.com/isaradhi24/Deploy-to-k8s-using-jenkins-e2e-CICD'
          }
    }
    stage("Building Application"){
          steps{
            sh "mvn clean package"
          }
    }
    stage("Test the application"){
      steps{
        sh "mvn test"
      }
    }
    stage (""){
      
    }
  }
}