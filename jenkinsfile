
pipeline {
  agent {
    docker { 
    image 'node:16-alpine'
    args '-u root'
    alwaysPull true
    reuseNode true
     }
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm-install'
      }
    }
  }
}
