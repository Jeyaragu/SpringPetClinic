node {
     tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "MAVEN_HOME"
    }
    stage('clone') {
        git branch:'main', url: 'https://github.com/Jeyaragu/SpringPetClinic.git'
    }
    stage('Compilation') {
        bat './mvn clean install -DskipTests=true'
    }
    stage('deployment') {
        archiveArtifacts 'target/*.jar'
    }
}
