pipeline {
  agent {
    label 'ubuntu'
  }
  stages {
    stage('Build') {
      post {
        success {
          sh 'echo Funciona'
        }

      }
      steps {
        sh 'cat /etc/os-release'
        sh 'ps -ef'
        git 'https://github.com/jglick/simple-maven-project-with-tests.git'
        container(name: 'ubuntu') {
          sh 'cat /etc/os-release'
          sh 'apt --version'
        }

      }
    }

    stage('Test') {
      steps {
        sh 'echo Soy un test'
      }
    }

  }
}
