#!/user/bin/env groovy

import io.jenkins.plugins.casc.ConfigurationAsCode;

pipeline {
  agent any

  environment {
    CASC_JENKINS_CONFIG = './casc_configs'
  }

  stages {
    stage('checkout') {
      steps {
        checkout scm
      }
    }

  // stages {
  //   stage('set casc_configs path') {
  //     steps {
  //       checkout scm
  //     }
  //   }

    stage('reload jcasc') {
      steps {
        ConfigurationAsCode.get().configure()
      }
    }
  }
  
}
