pipeline {
  agent {label 'NPM'}
  stages {
    stage('git clone') {
      steps {
        git url: 'https://github.com/99876543/js-e2e-express-server.git',
            branch: 'declarative'
      }
    }
    stage('Build') {
      steps {
        sh 'npm install' 
        sh 'npm run build' 
      }
    }
    stage('Test') {
      steps {
        sh 'npm test' 
      }
    }
    stage('Update') {
      steps {
        sh 'npm update'
      }
    }
  }
}
