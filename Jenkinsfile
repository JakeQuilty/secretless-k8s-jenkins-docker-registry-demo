pipeline {
  environment {
    registry = "YourDockerhubAccount/YourRepository"
    registryCredential = 'dockerhub_id'
    dockerImage = ''
  } 
  agent any
  stages {
    stage('Listing Repo Images') {
      steps {
        sh './bin/list-private-registry.sh'
      }
    }
    stage('Tests') {
      steps{
        sh './bin/test.sh'
      }
    }
    stage('Cleaning up') {
      steps{
        sh "echo DONE!!"
      }
    }
  }
}
