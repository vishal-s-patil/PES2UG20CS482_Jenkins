pipeline {
  agent any
  stages {
    stage('Build'){
      steps {
        sh 'g++ working.cppp'
        build job: "PES2UG20CS482-1", wait: true
      }
    }
    stage('Test'){
      steps{
        sh './a.out'
      }
    }
  }
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
