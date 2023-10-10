pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'echo "Building..."'

        // Add a dir step to navigate to the workspace directory
        dir("/var/lib/jenkins/workspace") {
          // Use grep to search for @tmp and _ws_cleanup patterns in files
          sh 'grep -rl "@tmp" . > tmp_files.txt'
          sh 'grep -rl "_ws_cleanup" . > cleanup_files.txt'

          // Use a while loop to delete files with @tmp extension
          sh 'while read -r file; do rm -rf "$file"; done < tmp_files.txt'
          
          // Use a while loop to delete files with _ws_cleanup extension
          sh 'while read -r file; do rm -rf "$file"; done < cleanup_files.txt'
          
          // Cleanup temporary files
          sh 'rm -f tmp_files.txt cleanup_files.txt'
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
