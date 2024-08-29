pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'Raiyan-sharif', url: 'https://github.com/Raiyan-sharif/python_jenkins_demo_project.git']])
      }
    }
    stage('Build') {
      steps {
        git branch: 'main', credentialsId: 'Raiyan-sharif', url: 'https://github.com/Raiyan-sharif/python_jenkins_demo_project.git'
        sh 'python3 hello.py'
      }
    }
    stage('Test') {
      steps{
        sh 'python3 test_hello.py'
       }
    }
  }
}