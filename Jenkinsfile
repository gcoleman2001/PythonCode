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
      }
    }
  }
}