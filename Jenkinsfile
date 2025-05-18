pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', url: 'https://github.com/NITHESH-MP/Maven_Build_Optimization'
      }
    }

    stage('Build with Maven') {
      steps {
        sh 'mvn -T 4 clean install -DskipTests'
      }
    }
  }

  post {
    success {
      echo '✅ Build succeeded!'
    }
    failure {
      echo '❌ Build failed.'
    }
  }
}
