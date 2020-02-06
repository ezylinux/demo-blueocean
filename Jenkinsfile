pipeline {
  agent any
  stages {
    stage('Pull code') {
      when {
        expression {
          !env.BRANCH_NAME.contains("HotFix")
        }
      }
      steps {
          sh 'echo "feature-1"' 
      }   
    }
    stage('Build') {
      when {
        not {
          branch 'master'
        }
      }
      steps {
        sh 'echo "build"'
        
      }
    }
  }
}
