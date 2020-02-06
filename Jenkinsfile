pipeline {
  agent any
  stages {
    stage('Pull code') {
      steps {
        if (env.BRANCH_NAME == 'feature-1') {
          sh 'echo "feature-1"' 
        }
        sh 'printenv'
          
      }
    }
    stage('Build') {
      steps {
        sh 'echo "build"'
        
      }
    }
  }
}
