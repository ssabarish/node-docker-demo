pipeline {
  agent any
  stages {
    stage('git') {
      steps {
        sh '''cd /home/s/new/node-docker-demo
git checkout start-here
git pull'''
      }
    }
  }
}