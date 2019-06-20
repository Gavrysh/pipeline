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
		emailext body: 'A Test EMail',
		recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']],
		subject: 'Test',
		to: 'abc'
	}
  }
}