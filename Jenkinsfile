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
        sh 'docker build -t shivaraj/docker-react -f Dokerfile.dev .'
      }
    }
    
    stage('run image') {
      steps {
        // docker run
        sh 'docker run -d -p 8080:8080 shivaraj/docker-react '
      }
    }
    
    
  }
}
