pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'cd ./example-react; npm install; npm start'
      }
    }

    stage('Test') {
      steps {
        sh 'cd ./example-react; npm run test -- --coverage --watchAll=false'
      }
    }

    stage('Deploy') {
      steps {
        sh 'cd ./example-react; npm run build'
      }
    }

  }
}