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
    stage('Deploy'){
      steps{
        echo 'Deploy'
      }
    }
  }
  post {
    failure {
      echo 'pipeline failed'
    }
  }
}
