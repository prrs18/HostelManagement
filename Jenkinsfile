pipeline {
  agent any
  stages {
    stage('verify version') {
      steps {
        sh 'php --version'
      }
    }
    stage('Clone Repository') {
            steps {
                script {
                    // Clean up any existing workspace
                    deleteDir()

                    // Clone the Git repository
                    sh "git clone https://github.com/prrs18/HostelManagement.git /var/www/html/code"
                }
            }
        }
    stage('hello') {
      steps {
        sh 'php index.php'
      }
    }
  }
}
