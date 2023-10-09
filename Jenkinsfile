pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Building..."'

        // Add a dir step to navigate to the workspace directory
        
        sh 'cd /var/lib/jenkins/workspace/cleanup@tmp'
          // Use sh to run the rm command to delete folders with @tmp extension
       sh 'find . -type d -name "*@tmp" -exec rm -rf {} +'

        
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
