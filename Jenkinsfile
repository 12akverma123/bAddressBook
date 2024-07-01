pipeline {
    agent any

//      tools {
//              jdk 'jdk11'
//      }
//      environment {
//              M2_INSTALL = "/usr/bin/mvn"
//      }

    stages {
        stage('Clone-Repo') {
                steps {
                        checkout scm
                }
        }
        stages('find username'){
                steps{
                    username
                    pwd
                    ls
                }
        }

        
    }
}
