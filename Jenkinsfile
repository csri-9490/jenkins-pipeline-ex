pipeline {
  agent any
  stages {
    stage('Hello') {
     steps {
       sh 'echo Hello world'
       mail bcc: '', body: 'Test', cc: '', from: '', replyTo: '', subject: 'Test', to: 'srikanthchelukala@gmail.com'
     }
   }
     stage('Hello1') {
        steps {
          sh 'echo Hello world12'
          emailext body: 'Test', subject: 'Test', to: 'srikanthchelukala@gmail.com'
        }
     }
 }
}