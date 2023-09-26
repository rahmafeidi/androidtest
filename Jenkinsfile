pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo "building"
        sleep 10
      } 
    }
    stage('Test') {
      steps {
        sh './gradlew '
      }
    }
    stage('Deploy') {
      steps {
        echo "deploying"
        sh './gradlew build '
        sh './gradlew clean build '
        sh './gradlew test '
      }
    }
  }
}
