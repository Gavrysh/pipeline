pipeline {
  agent {
    node {
        label 'ubuntu'
    }
  }
  stages {
    stage('Build') {
      steps {
        echo 'Build ...'
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
		recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']]
	}
  }
}