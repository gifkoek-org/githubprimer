pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'git@github.com:gifkoek-org/githubprimer.git', branch: 'main', credentialsId: 'aacorne-jenkins', poll: true)
      }
    }

  }
}