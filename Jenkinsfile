pipeline {
  agent any
  stages {
    stage('Pull code') {
      when {
        expression {
          env.BRANCH_NAME.contains("feature")
        }
      }
      steps {
          sh 'echo "feature-1"' 
          sh 'printenv'
      }   
    }
    stage('Build') {
      when {
        not {
          branch 'master'
        }
      }
      steps {
        sh 'echo "build" ; ls'
        sh 'printenv'
      }
    }
    stage('Build1') {
      when {
          branch 'dev'
      }
      steps {
        sh 'echo "build" ; ls'
        sh 'printenv'
        
      }
    }    
  }
}
