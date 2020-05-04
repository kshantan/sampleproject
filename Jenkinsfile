pipeline {
  agent any
  stages {
    stage('sourcecode') {
      steps {
        git 'https://github.com/kshantan/sampleproject.git'
      }
    }

    stage('build') {
      steps {
        sh '''mvn -version

mvn clean install'''
      }
    }

  }
}