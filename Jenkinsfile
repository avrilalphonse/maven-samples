pipeline {
  agent any
  tools { 
      maven 'DHT_MVN' 
      jdk 'DHT_SENSE' 
  }
  stages {
    stage('check out') {
      steps {
        git(url: 'https://github.com/avrilalphonse/maven-samples', branch: 'master')
      }
    }

    stage('clean') {
      steps {
        bat 'mvn clean'
      }
    }

    stage('test') {
      steps {
        bat 'mvn test'
      }
    }

    stage('verify') {
      steps {
        bat 'mvn verify'
      }
    }

  }
}
