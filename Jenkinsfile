#!/user/bin/env groovy

import io.jenkins.plugins.casc.ConfigurationAsCode;

pipeline {
  agent any

  stages {
    stage('checkout') {
      steps {
        checkout scm
      }
    }

    stage('reload jcasc') {
      steps {
        echo "${env.CASC_JENKINS_CONFIG}"
        // ConfigurationAsCode.get().configure()
      }
    }
  }
  
}
