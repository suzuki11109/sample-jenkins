node {
  checkout scm

  stage('Build') {
    echo "Hello from Jenkinsfile"
  }

  stage('Test') {
    sh 'make check || true'
  }

  stage('Deploy') {
    echo currentBuild.result
    if (currentBuild.result == 'SUCCESS') {
      echo "Deploy success"
    }
  }
}
