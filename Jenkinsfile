#!/user/bin/env groovy

import io.jenkins.plugins.casc.ConfigurationAsCode;

pipeline {
  agent any

  environment {
    CASC_JENKINS_CONFIG = "$JENKINS_HOME/casc_configs"
  }

  stages {
    stage('checkout') {
      steps {
        checkout scm
      }
    }

  stages {
    stage('install configs') {
      steps {
        sh "mv casc_configs $JENKINS_HOME"
      }
    }

    stage('reload jcasc') {
      steps {
        echo "$JENKINS_HOME/casc_configs"
        sh "ls $JENKINS_HOME/casc_configs"
        // ConfigurationAsCode.get().configure()
      }
    }
  }
  
}
