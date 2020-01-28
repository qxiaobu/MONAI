pipeline {
  agent {
    docker {
      image 'nvcr.io/nvidia/pytorch:19.10-py3'
      args 'stages: '
    }

  }
  stages {
    stage('Test') {
      steps {
        sh 'cat README.md'
      }
    }
  }
}