node {
  checkout scm

  stage('Build') {
    echo "Hello from Jenkinsfile"
  }

  stage('Test') {
    try {
        sh "exit 1"
        currentBuild.result = 'SUCCESS'
    } catch (Exception err) {
        currentBuild.result = 'FAILURE'
    }
    echo "RESULT: ${currentBuild.result}"
  }

  stage('Deploy') {
    if (currentBuild.result == 'SUCCESS') {
      echo "Deploy success"
    } else {
      echo "Deploy failed"
    }
  }
}
