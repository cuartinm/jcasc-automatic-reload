#!/user/bin/env groovy

import io.jenkins.plugins.casc.ConfigurationAsCode;

node {
  try { 
    checkout()
    env.CASC_JENKINS_CONFIG="${JENKINS_HOME}/casc_configs" 
    setUp()
    loadConf() 
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
def setUp() {
  stage('Install Configs') {
    sh """rm -rf ${JENKINS_HOME}/casc_configs
          mv ./casc_configs ${JENKINS_HOME}
          chmod 447 ${CASC_JENKINS_CONFIG}/*
          cat ${CASC_JENKINS_CONFIG}/*
          env"""
  }
}
def loadConf() {
  stage('Relaod JCasC') {
    ConfigurationAsCode.get().configure()
  }
}
