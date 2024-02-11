pipeline {
  agent any
  stages {
    stage('verify version') {
      steps {
        sh 'php --version'
      }
    }
    stage('Change Directory Permissions') {
            steps {
                script {
                    // Change permissions of the directory to allow Jenkins write access
                    sh "sudo chmod -R 775 /var/www/html"
                }
            }
        }
    stage('Clone Repository') {
            steps {
                script {
                    // Clean up any existing workspace
                    deleteDir()

                    // Clone the Git repository
                    sh "git clone https://github.com/prrs18/HostelManagement.git /var/www/html/intern"
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
