pipeline {
  agent {
    kubernetes {
      yamlFile 'KubernetesPod.yaml'
    }
  }
  stages {
    stage('Build') {
      steps {
        container('kaniko') {
          sh '''
          /kaniko/executor -f `pwd`/Dockerfile -c `pwd` --cache=true --destination=index.docker.io/zhan9san/test-kaniko:latest
          '''
        }
      }
    }
  }
}
