pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        sh 'g++ working.cpp'
        build job: "PES2UG20CS482-1", wait: true
      }
    }
    stage('Test'){
        sh './a.out'
    }
  }
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
