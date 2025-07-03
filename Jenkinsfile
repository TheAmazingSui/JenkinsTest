pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(credentialsId: 'github-sui', url: 'https://github.com/TheAmazingSui/JenkinsTest', branch: 'main')
      }
    }

    stage('Shell script') {
      parallel {
        stage('Shell script') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-end test') {
          steps {
            sh '''cd curriculum-app
cd curriculum-front && npm i && npm run test:unit'''
          }
        }

      }
    }

  }
}