pipeline {
    agent any
    tools {
    gradle "Gradle_1"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon --warning-mode all'
                // archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
                   
        }
   }
