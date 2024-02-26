node {
    stage('clone') {
        git branch:'main', url: 'https://github.com/Jeyaragu/SpringPetClinic.git'
    }
    stage('Compilation') {
        bat 'mvn clean install'
    }
    stage('deployment') {
        archiveArtifacts 'target/*.jar'
    }
}