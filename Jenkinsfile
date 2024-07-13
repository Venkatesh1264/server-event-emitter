node {
  stage("Clone the project") {
    git branch: 'master', url: 'https://github.com/Venkatesh1264/server-event-emitter.git'
  }

  stage("Compilation") {
    sh "./mvnw clean install -DskipTests"
  }

  stage("Tests and Deployment") {
    stage("Runing unit tests") {
      sh "./mvnw test -Punit"
    }
  }
}