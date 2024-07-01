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
        stage('find username'){
                steps {
                    username
                    pwd
                }
        }

        
    }
}
