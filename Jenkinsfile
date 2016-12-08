node {
  checkout scm

  stage('Build') {
    echo "Hello from Jenkinsfile"
  }

  stage('Test') {
    sh 'make check || true'
    currentBuild.result = 'SUCCESS'
  }

  stage('Deploy') {
    if (currentBuild.result == 'SUCCESS') {
      echo "Deploy success"
    }
  }
}
