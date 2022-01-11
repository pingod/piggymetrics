pipeline {
  agent {
    docker {
      image 'maven:alpine'
    }

  }
  stages {
    stage('') {
      steps {
        container(name: 'mvn', shell: 'mvn clean package -Dmaven.skip.test=true -U')
      }
    }

  }
}