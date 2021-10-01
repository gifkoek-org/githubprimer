pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'git@github.com:gifkoek-org/githubprimer.git', branch: 'main', credentialsId: 'aacorne-jenkins', poll: true)
      }
    }
    
    stage('prep') {
        steps {
            script {
                sh '''
                    apt update && apt install awscli
                '''
            }
        }
    }

    stage('build') {
        steps {
            script {
                sh '''
                    pwd
                    ls -la
                    echo ${GIT_COMMIT}
                    aws s3 ls
                '''
            }
        }
    }
  }
}