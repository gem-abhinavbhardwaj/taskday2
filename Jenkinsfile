pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Building..."'

       
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
        dir("/var/lib/jenkins/workspace") {
          // Use find to locate folders with @tmp extension and delete them
          sh 'ls'
          find . -type d \( -name "*@tmp" -o -name "*_ws_cleanup" \) -exec rm -rf {} +
          sh 'ls'
      }
    }
  }
}
}
  
