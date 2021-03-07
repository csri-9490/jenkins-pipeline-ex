pipeline {
   agent any

   environment {
      SURL = "globale.example.com"
   }
   stages {
     stage('Hello') {
       environment {
         SURL = "local.example.com"
       }
       steps {
           sh 'echo $(SURL)'
       }
     }
     stage('Hello1') {
         steps {
            echo 'hello world1'
         }
     }

   }
}
