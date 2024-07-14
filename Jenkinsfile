pipeline {
    agent any
    tools {
      maven 'Maven-3.9.8'
      jdk 'JDK 17'
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

    post {
        always {
            cleanWs()
        }
        success {
            echo 'Build successful!'
        }
        unstable {
            echo 'Build unstable.'
        }
        failure {
            echo 'Build failed!'
        }
    }
}