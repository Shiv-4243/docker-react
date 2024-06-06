pipeline {
  agent any
  
  stages {
    stage('Git Checkout') {
      steps {
        // Git checkout
        git branch: 'main', url: 'https://github.com/Shiv-4243/docker-react.git'
      }
    }
    
    stage('build image') {
      steps {
        // build image
        bat 'docker build . -t shivaraj/docker-react'
      }
    }
    
    stage('run image') {
      steps {
        // docker run
        bat 'docker run -d -p 8000:8000 shivaraj/docker-react'
      }
    }
    
    
  }
}
