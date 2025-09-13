pipeline {
  agent any
  triggers { pollSCM('H/5 * * * *') } // Check GitHub every 5 mins
  stages {
    stage('Stage 1: Build') {
      steps { echo 'Task: Compile | Tool: Maven' }
    }
    stage('Stage 2: Unit Tests') {
      steps { echo 'Task: Run tests | Tool: JUnit' }
    }
    stage('Stage 3: Code Analysis') {
      steps { echo 'Task: Static analysis | Tool: SonarQube' }
    }
    stage('Stage 4: Security Scan') {
      steps { echo 'Task: Security scan | Tool: Snyk' }
    }
    stage('Stage 5: Deploy to Staging') {
      steps { echo 'Task: Deploy staging | Tool: Docker' }
    }
    stage('Stage 6: Staging Tests') {
      steps { echo 'Task: Integration test2 | Tool: Postman' }
    }
    stage('Stage 7: Deploy to Production') {
      steps { echo 'Task: Deploy prod | Tool: Kubernetes' }
    }
  }
}
