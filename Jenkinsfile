pipeline {
    agent any
    tools {
      maven 'MAVEN_HOME'
      jdk 'JAVA_HOME'
    }
    stages {
      stage("Clone the project") {
        steps {
            git branch: 'master', url: 'https://github.com/Venkatesh1264/server-event-emitter.git'
        }
      }
      stage ('Build') {
        steps {
          bat 'mvn clean install'
        }
      }
      stage("Tests and Deployment") {
          steps {
            bat "mvn test -Punit"
          }
      }
    }
}