pipeline {
  agent any
  
  tools {
    gradle 'Gradle-7.5'
  }
  
  stages {
    stage("run frontend") {
      steps {
        echo 'executing yarn...'
        nodejs('Node-18.1.0') {
          bash 'yarn install'
        }
      }
    }
    stage('run backend') {
      steps {
        echo 'executing gradle...'
        bash './gradlew -v'
      }
    }
  }
}
  
