pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Building..."'

        // Add a dir step to navigate to the workspace directory
        dir("${env.Jenkins}") {
          // Use sh to run the rm command to delete folders with @tmp extension
          sh 'rm -rf *@tmp'
        }
      }
    }
    stage('Test') {
      steps {
        sh 'echo "Testing..."'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying..."'
      }
    }
  }
}
