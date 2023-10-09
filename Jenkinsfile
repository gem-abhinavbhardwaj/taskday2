pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Building..."'
         sh "cd ${env.WORKSPACE}"
          // Use find to locate folders with @tmp extension and delete them
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
