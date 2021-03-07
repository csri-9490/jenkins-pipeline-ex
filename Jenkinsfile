pipeline {
   agent any

   environment {
      SURL = "globale.example.com"
   }
   options {
      disableConcurrentBuilds()
   }
   //triggers {
    // cron('* * * * *')
   //}
   triggers {
       pollSCM('* * * * *')
   }
   tools {
           nodejs 'node-15'
   }
   parameters {
           string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
           text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
           booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
           choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
           password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
   }
   stages {
     stage('Hello') {
       environment {
         SURL = "local.example.com"
       }
       steps {
         sh 'node --version'
       }
       //steps {
       //    sh 'echo ${SURL}'
       //    sh 'person name= ${PERSON}'
       //}

     }
     stage('Hello1') {
        input {
           message "Should we continue?"
           ok "Yes, we should."
           submitter "alice,bob"
        }
                                                    }
        steps {
            echo 'hello world1'
        }
     }

   }
}
