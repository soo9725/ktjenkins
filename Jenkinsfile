pipeline {
  agent any
  stages {
    stage('git clone or git pull') {
      steps {
        git url: 'https://github.com/soo9725/ktjenkins.git', branch: 'master'
      }
    }
    stage ('CD using k8s'){
      steps {
        sh '''
        kubectl apply -f testapp.yml
        '''
      }
    }
  }
}