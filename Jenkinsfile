#!/user/bin/env groovy
​
import io.jenkins.plugins.casc.ConfigurationAsCode;
​
node {
  withEnv(["CASC_JENKINS_CONFIG=${JENKINS_HOME}/casc_configs"])
  try { 
    checkout()
    setUp()
    loadConf() 
  } catch(Exception e) {
    currentBuild.result = 'FAILURE'
  } finally {
      cleanWs()
  }
}
​
def checkout() {
    stage('Checkout') {
        checkout scm
    }
} 
​
def setUp() {
    stage('Install Configs') {
        sh """rm -rf ${JENKINS_HOME}/casc_configs && \\
            mv ./casc_configs ${JENKINS_HOME}"""
    }
}
​
def loadConf() {
    stage('Relaod JCasC') {
        // ConfigurationAsCode.get().configure()
    }
}
