pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        sh 'python3 -m pip install --user --upgrade pip && python3 -m pip uninstall -y torchvision && python3 -m pip install --user -r requirements.txt && python3 -m pip install --user flake8 pep8-naming && python3 -m pip list'
        sh 'python3 -m flake8 . --count --select=E9,F63,F7,F82 --show-source --statistics --config ./.flake8'
        sh './runtests.sh --net'
      }
    }

  }
}