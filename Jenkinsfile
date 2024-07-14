node {
  stage("Clone the project") {
    git branch: 'master', url: 'https://github.com/Venkatesh1264/server-event-emitter.git'
  }

  stage("Compilation with new changes") {
    bat 'mvn clean compile'
  }

  stage("Tests and Deployment") {
    stage("Runing unit tests") {
      bat "./mvnw test -Punit"
    }
  }
}