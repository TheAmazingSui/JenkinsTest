pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(credentialsId: 'github-sui', url: 'https://github.com/TheAmazingSui/JenkinsTest', branch: 'main')
      }
    }

    stage('Shell script') {
      steps {
        sh 'ls -la'
      }
    }

  }
}