pipeline {
  agent any

  stages{
    stage('Checkout Code') {
      steps {
        echo 'Pulling code from Github'
        checkout scm
      }
    }
    stage('Build Docker Image') {
      steps {
        echo 'Building Docker Image'
        bat 'docker build -t company1-website .'
      }
    }
    stage('Run docker conatainer') {
      steps {
        echo 'Running Docker container'
        bat 'docker run -d -p 8070:80 company1-website'
  }
}
}
}
