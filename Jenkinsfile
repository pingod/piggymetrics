pipeline {
  agent none
  stages {
    stage('1') {
      agent {
        docker {
          image 'mven:alpine'
        }

      }
      steps {
        sh 'mvn clean package -Dmaven.skip.test=true -U'
      }
    }

  }
}