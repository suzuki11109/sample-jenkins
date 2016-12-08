node {
  checkout scm

  stage('Build') {
    echo "Hello from Jenkinsfile"
  }

  stage('Deploy') {
    if (currentBuild.result == 'success') {
      echo "Deploy success"
    }
  }
}
