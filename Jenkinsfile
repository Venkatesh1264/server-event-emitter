node {
  stage("Clone the project") {
    git branch: 'master', url: 'https://github.com/Venkatesh1264/server-event-emitter.git'
  }

  stage("Compilation with new changes") {
    bat 'mvn clean install'
  }

  stage("Tests and Deployment") {
    stage("Runing unit tests") {
      bat "mvn test -Punit"
    }
  }
}