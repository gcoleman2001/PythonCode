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
        stage('Run the python script') {
          steps {
            powershell(script: 'python Casting.py', returnStatus: true)
          }
        }
      }
    }
  }
}