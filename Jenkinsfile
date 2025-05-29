pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/amrutha0404/devrepo1', branch: 'master', credentialsId: 'd4dd91a4-47d6-4a0e-9745-d0f570ec0003	')
        sh '''sudo docker build -t amru44/jrepo1:latest
sudo docker push mru44/jrepo1:latest '''
      }
    }

    stage('Deploy') {
      steps {
        sh 'sudo docker run -d -p 7777:8080 amru44/jrepo1:latest'
      }
    }

  }
}