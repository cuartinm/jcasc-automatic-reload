#!/user/bin/env groovy

import io.jenkins.plugins.casc.ConfigurationAsCode



node {
  try {
    checkout()
  } catch(Exception e) {
    currentBuild.result = 'FAILURE'
  } finally {
      cleanWs()
  }
}


def checkout() {
    stage('Checkout') {
        checkout scm
    }
}

// pipeline {
//   agent any

//   environment {
//     CASC_JENKINS_CONFIG = ""
//   }

//   stages {

//     stage('checkout') {
//       steps {
//         checkout scm
//       }
//     }

//     stage('install configs') {
//       steps {
//         sh "rm -rf $JENKINS_HOME/casc_configs"
//         sh "mv ./casc_configs $JENKINS_HOME"
//       }
//     }

//     stage('reload jcasc') {
//       steps {
//         ConfigurationAsCode.get().configure()
//       }
//     }
    
//   }
  
// }
