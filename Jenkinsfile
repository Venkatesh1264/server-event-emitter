node {
  stage("Clone the project") {
    git branch: 'master', url: 'https://github.com/Venkatesh1264/server-event-emitter.git'
  }

  stage("Compilation with new changes") {
    sh "mvn -B -DskipTests clean package"
  }

  stage("Tests and Deployment") {
    stage("Runing unit tests") {
      sh "./mvnw test -Punit"
    }
  }
}