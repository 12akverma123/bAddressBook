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

        stage('Build') {
            steps {
                sh 'mvn install -Dmaven.test.skip=true'
            }
        }

        stage('Unit Tests') {
            steps {
                sh 'mvn compiler:testCompile'
                sh 'mvn surefire:test'
                junit 'target/**/*.xml'
            }
        }

        stage('Deployment') {
            steps {
                sh 'sshpass -p "staaragile" scp target/addressbook.war staaragile@172.31.40.32:/home/staragile/apache-tomcat-9.0.85/webapps'
            }
        }
    }
}
