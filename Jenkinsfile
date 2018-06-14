pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh '''echo $HIDE_ME
sudo npm install'''
      }
    }
  }
  environment {
    REALLY_SECURE = 'BetterNotShow'
    HIDE_ME = credentials('FNID_APP_ID_DEV')
  }
}
