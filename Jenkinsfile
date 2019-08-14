pipeline {
  agent any
  tools {
    maven 'maven 3.3.9'
    jdk 'jdk8'
  }
  stages {
    agent { docker 'maven:3-alpine' }
    stage ('Build') {
      steps {
        echo 'This is a Build stage.'
        sh 'mvn -B clean package'
        archiveArtifacts artifacts: '**/target/*.jar',
          fingerprint: true
        
      }
    }
  }
}
