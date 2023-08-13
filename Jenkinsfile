pipeline {
    agent any   
    stages {
        stage("run frondend"){
            steps {
                echo 'executing yarn'
                nodejs('node_10_17'){
                    sh 'yarn install'
                }
            }
        }
        stage("run backdend"){
            steps {
                echo 'executing gradle'
                withGradle(){
                    sh './gradlew -v'
                }
            }
        }
                   
        }
   }
