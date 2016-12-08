node {
  checkout scm

  stage('Build') {
    echo "Hello from Jenkinsfile"
  }

  stage('Test') {
    sh 'make check || true'
  }

  stage('Deploy') {
    echo currentBuild
    if (currentBuild.result == 'SUCCESS') {
      echo "Deploy success"
    }
  }
}
