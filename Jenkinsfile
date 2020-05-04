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

    stage('undeploy') {
      steps {
        sh '''sudo rm -rf /*.war /usr/share/tomcat/webapps/
'''
        sleep 10
      }
    }

    stage('deploy') {
      steps {
        sh 'sudo cp -R  target/*.war  /usr/share/tomcat/webapps/'
      }
    }

  }
}