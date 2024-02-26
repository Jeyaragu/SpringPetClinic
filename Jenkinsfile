pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "MAVEN_HOME"
    }

    stages {
        stage('checkout') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/jglick/simple-maven-project-with-tests.git'
            }
        }
        stage('build') {
            steps {
                // bat 'mvn clean install -DskipTests=true'
                bat 'mvn clean install -DskipTests=true'
            }
        }
        stage('test') {
            steps {
                echo 'Skipping test'
            }
        }
        stage('deployment') {
            steps {
                archiveArtifacts 'target/*.jar'
            }
        }
    }
}
