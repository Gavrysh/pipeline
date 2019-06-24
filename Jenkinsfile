pipeline {
  agent {
    node {
      label 'ubuntu'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            echo 'Build ...'
          }
        }
        stage('') {
          steps {
            sh 'sh \'./deploy.sh\''
          }
        }
      }
    }
    stage('Test') {
      steps {
        echo 'Test ...'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy ...'
      }
    }
  }
  post {
    success {
      emailext(body: '', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: '', to: 'abc')

    }

  }
}