pipeline {
  agent {
    docker {
      image 'maven:alpine'
    }

  }
  stages {
    stage('maven-build') {
      steps {
        container(name: 'mvn', shell: 'mvn clean package -Dmaven.skip.test=true -U')
      }
    }

  }
}