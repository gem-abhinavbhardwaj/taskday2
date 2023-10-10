pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Building..."'

        // Add a dir step to navigate to the workspace directory
        dir("/var/lib/jenkins/workspace") {
          // Use find to locate folders with @tmp extension and delete them
          sh 'ls'
          sh 'find . -type d -name "*@tmp" -exec rm -rf {} +'
          sh 'ls'
          
          // Use find to locate files with @tmp extension and delete them
          //sh 'find . -type f -name "*@tmp" -exec rm -f {} +'
        }
      }
    }
    stage('Test') {
      steps {
        sh 'echo "Testing..."'
        sh'ls'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploying..."'
        sh'ls'
      }
    }
  }
}
