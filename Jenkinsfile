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
          sh 'pwd; ls -la'
        }
      }
    }
  }
}
