pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Building..."'

        // Add a dir step to navigate to the workspace directory
        
      }
    }
    stage('Test') {
      steps {
        dir("${env.WORKSPACE}") {
          // Use find to locate folders with @tmp extension and delete them
          sh 'find . -type d -name "*@tmp" -exec rm -rf {} +'
        }
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
