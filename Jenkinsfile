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

  // stages {
  //   stage('set casc_configs path') {
  //     steps {
  //       checkout scm
  //     }
  //   }

    stage('reload jcasc') {
      steps {
        echo "$JENKINS_HOME/casc_configs"
        sh "ls $JENKINS_HOME/casc_configs"
        // ConfigurationAsCode.get().configure()
      }
    }
  }
  
}
