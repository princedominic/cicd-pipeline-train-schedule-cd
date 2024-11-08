pipeline {
    agent any
    environment {
        JAVA_HOME = '/usr/bin/java'  // Replace with the actual path to your Java 11 installation
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
