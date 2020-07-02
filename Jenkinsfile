#!/user/bin/env groovy


pipeline {
  agent any

  stages {
    stage('checkout') {
      steps {
        echo "checkout"
      }
    }
    stage('reload jcasc') {
      steps {
        echo "reload jcasc"
      }
    }
  }
  
}
// params = [
//     sourceRepo      : 'https://github.com/AvalCoeDevOps/devops-pipeline-java-gradle-example.git',
//     credentialsId   : 'leeroy-jenkins',
//     gradleBuildCmd  : 'clean build',
//     gradleTestCmd   : 'clean test' ,
//     gradleDeployCmd : 'deploy'
// ]

// node {
//     try {
//         //docker.image("gradle:6.5.0-jdk8") {
//             checkout(params.sourceRepo, params.CredentialsId)
//             build(params.gradleBuildCmd)
//             test(params.gradleTestCmd)
//             if(env.BRANCH_NAME=="master" || env.BRANCH_NAME=="develop") {
//                 runSonarScanner()
//                 deploy(params.gradleDeployCmd)
//             }
//       //}
//     } catch(Exception e) {
//         currentBuild.result = 'FAILURE'
//     } finally {
//         notifyBuild(currentBuild.result)
//         cleanWs()
//     }
// }

// def checkout(repo, credentials) {
//     stage('Checkout') {
//         checkout scm
//     }
// }

// def build(cmd) {
//     stage('Gradle Build') {
//         runGradleCmd(cmd)
//     }
// }

// def test(cmd) {
//     stage('Unit Tests') {
//         runGradleCmd(cmd)
//     }
// }

// def deploy(cmd) {
//     stage('Deploy') {
//         runGradleCmd(cmd)
//     }
// }

// def runGradleCmd(cmd) {
//     sh """chmod +x gradlew && \
//           ./gradlew ${cmd}"""
// }

// def runSonarScanner() {
//     stage('GradleScan') {
//         runGradleCmd("sonarqube")
//     }
// }

// def notifyBuild(currentBuild = 'SUCCESS') {
    
// }  
