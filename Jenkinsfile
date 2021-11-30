pipeline {
  agent {
    label 'master'
  }
  tools {
    maven 'M3'
  }
  stages {
    stage ('Checkout') {
      steps {
        git branch: 'main', url: 'https://github.com/AnjuMeleth/SpringPetClinic.git'
      }
    }
    stage ('Build') {
      steps {
        sh 'mvn compile'
      }
    }
    stage ('Test') {
      steps {
        sh 'mvn test'
      }
    }
  }
}
