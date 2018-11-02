pipeline {
  agent any
  stages {
    stage('git') {
      parallel {
        stage('git') {
          steps {
            sh '''cd /home/s/new/node-docker-demo
git checkout start-here
git pull'''
          }
        }
        stage('docker') {
          steps {
            sh '''cd /home/s/giri
cp Dockerfile customer_web/.
docker build -t giri/app-$(date +%Y-%m-%d) customer_web/.
docker run -p 8181:8080 -d giri/app-$(date +%Y-%m-%d)'''
          }
        }
      }
    }
  }
}