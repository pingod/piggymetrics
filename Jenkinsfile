pipeline {
  agent none
  stages {
    stage('maven-build') {
      agent {
        docker {
          image 'registry.cn-hangzhou.aliyuncs.com/sourcegarden/docker-maven-aliyun:jdk-8'
        }

      }
      steps {
        sh '''#mvn clean package -Dmaven.skip.test=true -U
              mvn clean package -Dmaven.test.skip=true'''
        archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
      }
      
    }

  }
}