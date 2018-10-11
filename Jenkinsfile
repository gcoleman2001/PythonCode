pipeline {
  agent any
  stages {
    stage('Find File') {
      parallel {
        stage('Find File') {
          steps {
            fileExists 'Casting.py'
          }
        }
        stage('Run') {
          steps {
            sh '''#!/bin/bash
python Casting.py'''
          }
        }
        stage('error') {
          steps {
            echo 'Processing pipeline'
          }
        }
        stage('') {
          steps {
            git(url: 'https://github.com/gcoleman2001/PythonCode', branch: 'master', poll: true)
          }
        }
      }
    }
  }
}