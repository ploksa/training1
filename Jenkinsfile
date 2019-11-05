pipeline {
    agent any
    stages {
        stage ('syntax') {
            steps {
               apk -y install python
               sh 'python -m py_compile program.py'
                  }
                         }
        stage ('testing') {
            steps {
               sh 'bash test.sh' 
                     }       
                      }         
        stage ('deploy') {
            steps {
              sh 'echo "upload na server"'
                  }
                         }              
           }
         } 
