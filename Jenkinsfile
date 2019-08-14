pipeline {
  agent any
  stages {
    stage('Build') {
      agent { docker 'maven:3-alpine' }
    }
  }
}
