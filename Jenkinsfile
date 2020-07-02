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

    // stage('install configs') {
    //   steps {
    //     sh "mv ./casc_configs $JENKINS_HOME"
    //   }
    // }

    stage('reload jcasc') {
      steps {
        sh "ls $CASC_JENKINS_CONFIG"
        // ConfigurationAsCode.get().configure()
      }
    }
    
  }
  
}
