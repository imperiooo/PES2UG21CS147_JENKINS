pipeline{
  agent any
  stages{
    stage('Build'){
      steps{
        build 'PES2UG21CS147-1'
        sh 'g++ main.cpp -o output'

      }
    }
    stage('Test'){
      steps{
      sh './out'
      }
    }
    stage('Deploy'){
      steps{
        echo 'deploy'
      }
    }
  }
  post{
    failure{
      error 'Pipeline failed'
    }
}
}
