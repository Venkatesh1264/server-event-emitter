pipeline {
    agent any
    tools {
      maven 'MAVEN_HOME'
      jdk 'JAVA_HOME'
    }
    stages {
      stage ('Build') {
        stage("Clone the project") {
            git branch: 'master', url: 'https://github.com/Venkatesh1264/server-event-emitter.git'
        }
        steps {
          bat 'mvn clean install'
        }
      }
      stage("Tests and Deployment") {
          stage("Runing unit tests") {
            bat "mvn test -Punit"
          }
      }
    }
}