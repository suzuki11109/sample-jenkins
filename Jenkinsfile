node {
  checkout scm

  stage('Build') {
    echo "Hello from Jenkinsfile"
  }

  stage('Test') {
    sh "exit 1"
  }

  stage('Deploy') {
    echo currentBuild.result
    if (currentBuild.result == 'SUCCESS') {
      echo "Deploy success"
    } else {
      echo "Deploy failed"
    }
  }
}
