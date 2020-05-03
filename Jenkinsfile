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
        sh '''M2_HOME=/production/apps/apache-maven-3.6.3       
export  PATH=$PATH:$M2_HOME/bin
echo $PATH
mvn -version
'''
      }
    }

  }
}