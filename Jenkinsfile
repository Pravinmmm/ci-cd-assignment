pipeline {
    agent any   
    stages {
         stage("run frondend"){
               steps {
              echo 'executing yarn'
                nodejs('node_12.13.1'){
                    sh 'yarn install'
         }
               }
         }
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
                   
        }
   }
