pipeline {
   agent {
       label "mietiqueta"
   }

   stages {
      stage('Build') {
         steps {
            git 'https://github.com/jglick/simple-maven-project-with-tests.git'
            container('centos') {
                sh "yum --version"
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
