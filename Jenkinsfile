pipeline {
   agent {
       label "miagente"
   }

   stages {
      stage('Build') {
         steps {
            sh "cat /etc/os-release"
            sh "ps -ef"
            git 'https://github.com/jglick/simple-maven-project-with-tests.git'
            container('ubuntu') {
              sh "cat /etc/os-release"
              sh "apt --version"
            }
         }

         post {
            success {
               sh "echo Funciona"
            }
         }
      }
      stage('Test') {
         steps {
            sh "echo Soy un test"
         }

      }
   }
}
