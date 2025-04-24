pipeline {
  agent any

  stages {
    stage('Clone Repository') {
      steps {
        git 'https://github.com/your/repo.git'
      }
    }

    stage('Build Docker Image') {
      steps {
        script {
          docker.build('react-app-image', './react-app')
        }
      }
    }

    stage('Run Docker Container') {
      steps {
        script {
          sh 'docker run -d -p 3000:80 react-app-image'
        }
      }
    }
  }
}
